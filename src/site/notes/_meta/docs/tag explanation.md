---
{"dg-publish":true,"permalink":"/meta/docs/tag-explanation/","noteIcon":"","updated":"2024-10-29T09:53:29.350-07:00"}
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