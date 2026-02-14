```rust

struct Developer {
    name: &'static str,
    location: &'static str,
    role: &'static str,
    interests: &'static [&'static str],
    stack: &'static [&'static str],
}

fn about_me() -> Developer {
    Developer {
        name: "Vehan Hemsara",
        location: "Plymouth, UK",
        role: "Mobile & Backend Engineer",
        interests: &[
            "shipping real products",
            "clean architecture",
            "privacy-focused systems",
            "NFC and payments",
        ],
        stack: &[
            "Flutter",
            "SwiftUI",
            "Go",
            "Rust",
            "NestJS",
            "PostgreSQL",
        ],
    }
}

fn main() {
    let me = about_me();

    println!("Hi, I'm {}", me.name);
    println!("Based in {}", me.location);
    println!("Role: {}", me.role);
    println!("Interests:");
    for i in me.interests {
        println!("- {}", i);
    }
    println!("Tech stack:");
    for t in me.stack {
        println!("- {}", t);
    }
}
```

