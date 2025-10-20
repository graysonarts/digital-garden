---
{"dg-publish":true,"permalink":"/meta/docs/complete-tag-system-documentation/","title":"Simplified Tag System Documentation","tags":["📍_MOC","📖_Documentation","🏷️_Tags"],"updated":"2025-10-20T08:23:09.516-07:00"}
---


# Simplified Tag System Documentation

## Overview

This document provides a streamlined guide to the tag system used throughout the Obsidian vault. The system focuses on content discovery while leveraging the PARA (Projects, Areas, Resources, Archives) folder structure for organization.

## Core Philosophy

- **Let PARA folders do organizational work** (Projects vs Areas vs Resources)
- **Tags are for discovery** (finding content by subject/domain)
- **Keep only what you actually use**

## Three Tag Categories

### 1. Content Maturity
**Purpose**: Track content lifecycle for processing workflow.

- `📥_New` - Unprocessed capture
- `🌱_Active` - Currently working on
- `🌲_Evergreen` - Polished reference content
- `📦_Archive` - Historical/completed

**Usage**: Every piece of content should have exactly one maturity tag (min: 1, max: 1).

### 2. Content Format
**Purpose**: What type of content is this?

- `📍_MOC` - Map of Content
- `🗒️_Note` - General notes
- `📖_Reference` - External resources/links
- `📋_Template` - Reusable templates
- `🎬_Script` - Screenplays
- `📚_Course` - Educational material
- `💻_Project_Doc` - Project documentation
- `☢️_Atomic` - Core concept notes
-

**Usage**: Every piece of content should have exactly one format tag (min: 1, max: 1).

### 3. Subject/Domain
**Purpose**: What is this about? (primary discovery mechanism)

- `🎬_Film` - Film/cinema
- `📸_Photography` - Photography
- `🎭_Screenwriting` - Script writing
- `🔧_Technical` - Programming/tech
- `🏢_Business` - Business/career
- `🎨_Creative` - Creative work/art
- `📝_Writing` - Writing/literature
- `🏆_Fitness` - Health/fitness
- `🍽️_Nutrition` - Food/recipes
- `🎓_Learning` - Education/skills
- `🏠_Home` - Home management
- `💰_Finance` - Financial planning
- `🌎_Travel` - Travel and Vacation
- `📍_META` - System File

**Usage**: Apply 1-3 subject tags based on content relevance (min: 1, max: 3).

### 4. Energy Investment Level
**Purpose**: Track energy investment for projects and areas in Energy Investment Portfolio.

- `💪_Active_Investment` - High energy investments (limit: 2-3 active projects)
- `🍀_Tending_Investment` - Medium energy investments (limit: 3-4 tending projects)
- `🧊_Frozen_Investment` - Low energy/maintenance mode (no limit)
- `⏳_Someday_Investment` - Dream investments (stored in `3-Resources/Someday` folder)

**Usage**: Apply exactly one energy investment tag to projects/areas you want to track in your Energy Investment Portfolio. The `_Investment` suffix distinguishes these from Content Maturity tags.

## Tagging Guidelines

### Tag Count Requirements

Every piece of content should have:
- **Content Maturity tag**: exactly 1 (📥_New, 🌱_Active, 🌲_Evergreen, or 📦_Archive)
- **Content Format tag**: exactly 1 (📍_MOC, 🗒️_Note, 📖_Reference, etc.)
- **Subject/Domain tags**: 1-3 based on content relevance
- **Energy Investment tag**: exactly 1 for projects/areas tracked in Energy Investment Portfolio (optional for other content)

**Validation**: The system will warn when tag counts fall outside these ranges.

### Tag Format
- Use underscores (`_`) instead of spaces or dashes
- Emojis provide visual distinction and quick recognition
- Descriptive text follows the emoji

### Common Tag Combinations

**Active Project Work**:
- `🌱_Active` + `💻_Project_Doc` + `🔧_Technical`

**Reference Material**:
- `🌲_Evergreen` + `📖_Reference` + `🔧_Technical`

**Creative Content**:
- `🌱_Active` + `🎬_Script` + `🎭_Screenwriting` + `🎨_Creative`

**Learning Notes**:
- `📥_New` + `🗒️_Note` + `🎓_Learning` + `🔧_Technical`

## Migration from Previous System

### Content Maturity Mapping
- `📥_New` → `📥_New`
- `🌱_Processing` / `💪_Active` / `📋_Planning` → `🌱_Active`
- `✅_Processed` / `✅_Done` / `🌲_Evergreen` → `🌲_Evergreen` or `📦_Archive`
- `🧊_Frozen` / `❌_Canceled` → `📦_Archive`

### Content Format Mapping
- Most content uses `🗒️_Note` or `📍_MOC`
- Keep only essential format tags from the previous system

### Subject/Domain Mapping
- Consolidate overlapping tags from Work Type, Life Areas, Content Domain into single subject tags
- Example: `💼_Client_Work` + `🔧_Technical` + `🔧_Technology` → just `🔧_Technical`

## Benefits of Simplified System

1. **Faster tagging**: 3 decisions instead of 12
2. **Better search**: Fewer overlapping tags = clearer results
3. **Less maintenance**: 30-40 tags total instead of 100+
4. **PARA integration**: Folder structure handles organization, tags handle discovery
5. **Clearer mental model**: Maturity + Format + Subject = everything you need

## Integration with PARA

- **Projects**: Use Content Maturity + Content Format + relevant Subject/Domain tags
- **Areas**: Use Content Maturity + Content Format + relevant Subject/Domain tags
- **Resources**: Use Content Maturity + Content Format + relevant Subject/Domain tags
- **Archives**: Use `📦_Archive` + original tags for reference

This simplified system focuses on content discovery while leveraging PARA folders for organizational structure.
