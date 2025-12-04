# metodo-clase

A blog project built with Sanity CMS.

## Overview

This is a Sanity Studio project configured for a blog. It includes schemas for blog posts, authors, categories, and rich text content.

## Features

- **Blog Posts**: Full-featured blog post schema with title, slug, excerpt, body, images, and categorization
- **Authors**: Author profiles with bio and image
- **Categories**: Post categorization system
- **Rich Text Editor**: Block content with support for headings, lists, links, and embedded images
- **Image Management**: Image upload with hotspot support and alt text

## Prerequisites

- Node.js (v14 or higher)
- npm or yarn
- A Sanity account (sign up at https://www.sanity.io)

## Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd metodo-clase
```

2. Install dependencies:
```bash
npm install
```

3. Initialize your Sanity project:
```bash
npx sanity init
```

This will:
- Connect to your Sanity account
- Create a new project or select an existing one
- Update the `projectId` in configuration files

Alternatively, you can manually update the `projectId` in:
- `sanity.config.ts`
- `sanity.cli.ts`

## Development

Start the development server:
```bash
npm run dev
```

The Sanity Studio will be available at `http://localhost:3333`

## Build

Build the studio for production:
```bash
npm run build
```

## Deploy

Deploy the studio to Sanity's hosting:
```bash
npm run deploy
```

## Project Structure

```
.
├── schemaTypes/          # Content schemas
│   ├── post.ts          # Blog post schema
│   ├── author.ts        # Author schema
│   ├── category.ts      # Category schema
│   ├── blockContent.ts  # Rich text schema
│   └── index.ts         # Schema exports
├── sanity.config.ts     # Sanity configuration
├── sanity.cli.ts        # CLI configuration
├── package.json         # Dependencies and scripts
└── tsconfig.json        # TypeScript configuration
```

## Schema Types

### Post
- **title**: Post title (required)
- **slug**: URL-friendly slug (required)
- **author**: Reference to author
- **mainImage**: Featured image with alt text
- **categories**: Array of category references
- **publishedAt**: Publication date
- **excerpt**: Short description
- **body**: Rich text content

### Author
- **name**: Author name (required)
- **slug**: URL-friendly slug
- **image**: Author photo
- **bio**: Author biography

### Category
- **title**: Category name (required)
- **slug**: URL-friendly slug
- **description**: Category description

## Usage

1. Start the studio with `npm run dev`
2. Create authors in the Authors section
3. Create categories in the Categories section
4. Create blog posts in the Blog Post section
5. Use the Vision plugin (included) to test GROQ queries

## Customization

You can customize the schemas by editing files in the `schemaTypes/` directory. After making changes, restart the development server to see the updates.

## Learn More

- [Sanity Documentation](https://www.sanity.io/docs)
- [GROQ Query Language](https://www.sanity.io/docs/groq)
- [Sanity Studio](https://www.sanity.io/docs/sanity-studio)

## License

ISC
