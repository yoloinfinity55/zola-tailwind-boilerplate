+++
title="15 - Zola section and blog"
date = 2025-10-03
+++

Here’s a simple explanation of how "sections" and "blogs" work in Zola.

  What is a Section?

  Think of your content folder as a filing cabinet. A section is simply a drawer (a
  folder) inside that cabinet that you create to organize your pages.

   * You could have a section for blog, another for projects, and another for about.
   * Each section automatically gets its own landing page that lists all the pages inside
     it. For example, all your blog posts will be listed at the /blog/ URL.

  How Zola Displays a Section

  When you visit a section's URL (like /blog/), Zola needs instructions on how to display
  that list of pages. These instructions are templates.

  Zola looks for a template in your templates folder in a specific order:

   1. A specific template: It first looks for a template with the same name as the section,
      like templates/blog.html.
   2. A generic template: If it can't find that, it looks for a generic fallback template
      named templates/section.html.
   3. The default page: If it finds neither, it gives up and shows you that basic, unstyled
      page you saw earlier.

  This is why our fix worked. We created section.html, giving Zola the generic
  instructions it needed to display your blog section correctly.

  So, What is a "Blog"?

  In Zola, a blog is not a special feature. It's just a common name for a section.

  You create a blog simply by creating a folder named content/blog/. Every Markdown file
  you put in that folder becomes a blog post.

  By combining a content/blog/ folder with a templates/section.html template, you get a
  fully functional blog.