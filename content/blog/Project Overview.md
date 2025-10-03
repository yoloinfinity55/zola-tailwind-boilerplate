+++
title = "Project Overview"
date = 2025-10-03
taxonomies = { tags = ["Zola", "Tailwind","Improvements"], categories = ["Tutorials"], authors = ["Yolo"], series = ["Getting Started"] }
weight = 1
+++

Project Overview

  This is a static website project built with Zola and styled using Tailwind CSS. It's a
  lean setup designed for creating a blog with features like taxonomies (tags, categories,
  authors), dark mode, and a responsive layout.

  Core Technologies & Architecture

   * Static Site Generator: Zola. The main configuration is in config.toml, which defines
     the site's title, base URL, and the taxonomy structure. The build_search_index flag is
     enabled, providing out-of-the-box search functionality.
   * CSS Framework: Tailwind CSS. It's used for all styling. The configuration in
     tailwind.config.js is set up to scan all .html templates and .md content files for used
     classes, allowing Tailwind to purge unused styles and generate an optimized style.css
     file.
   * Dependency Management: npm. package.json defines a single development dependency:
     tailwindcss. There are two main scripts:
       * npm run dev: To be used during development. It watches for CSS changes and rebuilds
         the stylesheet automatically.
       * npm run build: To be used for production builds. It creates a minified version of
         the stylesheet.

  Templating and Frontend

   * Base Template: templates/base.html is the master template for the entire site. It
     includes:
       * A responsive header with desktop and mobile navigation.
       * A main content block where individual pages are rendered.
       * A footer with copyright information.
       * The single link to the generated stylesheet: <link rel="stylesheet" 
         href="/style.css">.
   * Frontend Features: The site includes client-side JavaScript for modern features:
       * Dark Mode: A theme toggler allows users to switch between light and dark modes. The
         preference is saved in the browser's localStorage.
       * Mobile Menu: A hamburger menu provides navigation on smaller screens.
       * Active Navigation Highlighting: The current page's link in the navigation bar is
         automatically highlighted.

  Content Structure

   * Format: Content is written in Markdown files with TOML front matter (the section
     between +++).
   * Example (`content/blog/first-post.md`):
       * The front matter defines metadata like title, date, and taxonomies.
       * The taxonomies field is used to associate the post with tags, categories, authors,
         and series, which are defined in config.toml.
   * Organization: The content/ directory holds all the website's content, organized into
     sections (like blog and authors).

  In summary, this is a well-structured, modern static site boilerplate. The development
  workflow revolves around writing Markdown content and running the npm run dev script
  alongside Zola's development server to see changes live.