# Era YAML (`github.com/era-lang-official/yaml`)

Lightweight YAML configuration parser and serializer for Era.

## Features
- **Key-Value Mappings**: Parse single and multi-level indented dictionary trees.
- **Section Scoping**: Resolves nested properties like `server.port`.
- **Stringification**: Converts configurations back into clean YAML format.

## Usage
```era
import "github.com/era-lang-official/yaml";

fn main() {
    let raw = "server:\n  port: 8080\n".to_string();
    let doc = parse_yaml(raw).unwrap();
    println(doc.get("server.port".to_string()).unwrap()); // "8080"
}
```

