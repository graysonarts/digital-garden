---
{"dg-publish":true,"permalink":"/meta/docs/tag-explanation/"}
---


# processing status
- 📥 - New
- 🚧 - Ready to Process
-  🌱 - Processing
- ✅ - Processed
- 🌲 - Evergreen

```mermaid
stateDiagram-v2

	[*] --> 📥
	 📥 --> 🚧
	 📥 --> 🌱
	 🚧 --> 🌱
	 🌱 --> 🌲
	 ✅ --> 🌲
	 🌱 --> ✅
	 ✅ --> [*]
	 🌲 --> [*]
```
# content type
- 🕛 - Processing Note
- 🔗 - Reference
- 📰 - Article
- 📺 - Video
- 🎧 - Podcast
- 📖 - Book
- 🗒️ - Note
- 📍 - MOC

# list types
- 💼 - Company
- 👤 - Person
- 🎥 - Movie or Television Show
- ⚙️ - Gear

## client types
- 💰Marketing
- 🥗 Nutrition
- 💻️ Coding
# output type
- 🎬 - Video
- 🏙️ - Photo
- 📝 - Blog Post / Essay

# project status
- ☢️ - Active
- 🍀 - Tending
- 🧊 - Frozen
- Nothing - Done