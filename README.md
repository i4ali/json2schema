# 🔄 JSON to Schema Generator

[![Live Demo](https://img.shields.io/badge/demo-live-brightgreen)](https://json2schema.app)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Made with JavaScript](https://img.shields.io/badge/Made%20with-JavaScript-yellow.svg)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)

> Convert JSON to TypeScript interfaces, Python dataclasses, Java POJOs, Zod schemas, and GraphQL types instantly. Fast, private, and beautiful.

[**Try it now →**](https://json2schema.app)

---

## ✨ Features

### 🌐 **5 Language Support**
- **TypeScript** - Generate type-safe interfaces
- **Python** - Create dataclass definitions
- **Java** - Build POJO classes with getters/setters
- **Zod** - Runtime validation schemas
- **GraphQL** - GraphQL type definitions

### 🎨 **Beautiful Syntax Highlighting**
- Real-time color-coded JSON input
- Syntax-highlighted schema output for all languages
- VS Code-inspired dark theme
- Material Design color palette

### 🔒 **Privacy-First**
- **100% client-side processing** - your data never leaves your browser
- No servers, no storage, no tracking
- Works offline once loaded
- Open source and transparent

### ⚡ **Smart & Fast**
- Instant schema generation as you type
- Handles deeply nested objects
- Array type inference (including mixed types)
- Automatic type detection for primitives

### 🎯 **Developer-Friendly**
- One-click copy to clipboard
- Sample data for quick testing
- Clear button for easy reset
- Responsive design for all devices

---

## 🚀 Quick Start

### Online (Recommended)
Just visit [json2schema.app](https://json2schema.app) - no installation needed!

### Local Development
```bash
# Clone the repository
git clone https://github.com/yourusername/json2schema.git

# Navigate to directory
cd json2schema

# Open in browser (no build step required!)
open index.html
```

---

## 📖 Usage Examples

### Example 1: API Response to TypeScript

**Input JSON:**
```json
{
  "id": 123,
  "name": "John Doe",
  "email": "john@example.com",
  "isActive": true,
  "tags": ["developer", "typescript"]
}
```

**Generated TypeScript:**
```typescript
interface Root {
  id: number;
  name: string;
  email: string;
  isActive: boolean;
  tags: string[];
}
```

### Example 2: Nested Objects to Python

**Input JSON:**
```json
{
  "user": {
    "profile": {
      "firstName": "Alice",
      "age": 28
    }
  }
}
```

**Generated Python:**
```python
from dataclasses import dataclass

@dataclass
class Profile:
    firstName: str
    age: int

@dataclass
class User:
    profile: Profile

@dataclass
class Root:
    user: User
```

### Example 3: Arrays to Zod Schema

**Input JSON:**
```json
{
  "items": [
    { "id": 1, "name": "Item 1" },
    { "id": 2, "name": "Item 2" }
  ]
}
```

**Generated Zod:**
```typescript
import { z } from 'zod';

const itemSchema = z.object({
  id: z.number().int(),
  name: z.string(),
});

const rootSchema = z.object({
  items: z.array(itemSchema),
});
```

---

## 🛠️ Tech Stack

- **Frontend**: Vanilla JavaScript (ES6+)
- **Styling**: Tailwind CSS (via CDN)
- **Fonts**: Inter & JetBrains Mono (Google Fonts)
- **Architecture**: Single-page application, no build tools
- **Hosting**: Static HTML/CSS/JS (works anywhere!)

**Why no framework?**
- Faster load times
- No dependencies to maintain
- Easier to understand and contribute
- Works offline once cached

---

## 🎨 Supported Type Mappings

### JSON to TypeScript
| JSON Type | TypeScript Type |
|-----------|-----------------|
| string    | `string` |
| number (int) | `number` |
| number (float) | `number` |
| boolean   | `boolean` |
| null      | `any` |
| array     | `Type[]` |
| object    | `Interface` |

### JSON to Python
| JSON Type | Python Type |
|-----------|-------------|
| string    | `str` |
| number (int) | `int` |
| number (float) | `float` |
| boolean   | `bool` |
| null      | `Optional[Any]` |
| array     | `List[Type]` |
| object    | `@dataclass` |

### JSON to Java
| JSON Type | Java Type |
|-----------|-----------|
| string    | `String` |
| number (int) | `Integer` |
| number (float) | `Double` |
| boolean   | `Boolean` |
| null      | `Object` |
| array     | `List<Type>` |
| object    | `public class` |

---

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

### Ideas for Contributions
- [ ] Add more languages (Go, Rust, C#, Kotlin, Swift)
- [ ] Support for optional properties
- [ ] Export to file functionality
- [ ] Dark/Light theme toggle
- [ ] Custom naming conventions
- [ ] URL parameter support for sharing
- [ ] History/undo feature
- [ ] More validation options for Zod

### Development Workflow
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Make your changes
4. Test thoroughly
5. Commit with clear message (`git commit -m 'Add amazing feature'`)
6. Push to your branch (`git push origin feature/amazing-feature`)
7. Open a Pull Request

### Code Style
- Use ES6+ syntax
- Comment complex logic
- Keep functions small and focused
- Follow existing naming conventions
- Test all language outputs

---

## 📝 Changelog

### v1.0.0 (Current)
- ✅ Initial release
- ✅ Support for 5 languages (TypeScript, Python, Java, Zod, GraphQL)
- ✅ Syntax highlighting for input and output
- ✅ Nested object and array support
- ✅ Copy to clipboard
- ✅ Sample data
- ✅ Responsive design
- ✅ SEO optimization

### Roadmap
- [ ] More language support
- [ ] File upload/download
- [ ] Settings panel
- [ ] Keyboard shortcuts
- [ ] API endpoint (optional)

---

## 🐛 Known Issues

- Mixed array types may default to `any` in some cases
- Very deeply nested objects (>10 levels) may be slow
- Some edge cases with special characters in keys

Found a bug? [Open an issue](https://github.com/yourusername/json2schema/issues)!

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

```
MIT License

Copyright (c) 2025 json2schema.app

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## 🙏 Acknowledgments

- Inspired by the need for a privacy-first JSON converter
- Built with love for the developer community
- Thanks to all contributors and users!

---

## 📞 Support

- **Live Demo**: [json2schema.app](https://json2schema.app)
- **Issues**: [GitHub Issues](https://github.com/yourusername/json2schema/issues)
- **Discussions**: [GitHub Discussions](https://github.com/yourusername/json2schema/discussions)

---

## 🌟 Star History

If you find this project useful, please consider giving it a star on GitHub! ⭐

---

## 📊 Stats

![GitHub stars](https://img.shields.io/github/stars/yourusername/json2schema?style=social)
![GitHub forks](https://img.shields.io/github/forks/yourusername/json2schema?style=social)
![GitHub watchers](https://img.shields.io/github/watchers/yourusername/json2schema?style=social)

---

<div align="center">

**[Website](https://json2schema.app)** •
**[Documentation](https://json2schema.app)** •
**[Report Bug](https://github.com/yourusername/json2schema/issues)** •
**[Request Feature](https://github.com/yourusername/json2schema/issues)**

Made with ❤️ by developers, for developers

</div>
