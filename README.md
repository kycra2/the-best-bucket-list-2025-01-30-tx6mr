# The Best Bucket List Landing Page - Maintenance Guide

This guide will help you maintain and customize the Bucket List landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your main navigation and logo. To update:

1. **Logo Text:**
```html
<a href="#" class="text-2xl font-bold text-indigo-600">BucketList</a>
```
- Replace "BucketList" with your desired text
- The `text-2xl` class controls size
- `text-indigo-600` controls the color

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-indigo-600 transition-colors duration-300">Features</a>
    <!-- Additional menu items -->
</div>
```
- Update text between `>` and `</a>` for each menu item
- Keep the `href` attributes matching your section IDs

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6 leading-tight">The Best Bucket List</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12 leading-relaxed">Turn Dreams into Memories, One Adventure at a Time</p>
```
- Update heading text between `<h1>` tags
- Update subheading text between `<p>` tags
- Classes like `text-4xl` control responsive text sizing

### Feature Cards
Each feature card follows this structure:
```html
<div class="bg-white p-8 rounded-2xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="w-16 h-16 bg-indigo-100 rounded-full flex items-center justify-center mb-6">
        <i class="fas fa-star text-2xl text-indigo-600"></i>
    </div>
    <h3 class="text-xl font-bold text-gray-900 mb-4">Turn dreams into reality</h3>
    <p class="text-gray-600 leading-relaxed">Create your personalized bucket list...</p>
</div>
```
To modify:
1. Change icon by updating `fa-star` to any [Font Awesome](https://fontawesome.com/icons) icon name
2. Update heading text between `<h3>` tags
3. Update description text between `<p>` tags

## Managing Links

### Navigation Links
Current navigation links are:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
To update:
1. Change `href="#section-name"` to point to your new section
2. Ensure the section ID matches: `<section id="section-name">`
3. Update the text between `<a>` tags

### Call-to-Action Buttons
Located in hero and footer sections:
```html
<a href="https://thebestbucketlist.com" class="inline-block px-8 py-4 bg-indigo-600 text-white rounded-full">
```
To update:
1. Replace `https://thebestbucketlist.com` with your destination URL
2. Test the link thoroughly before deploying

### Social Media Links
Located in the footer:
```html
<div class="flex space-x-4">
    <a href="#" class="hover:text-white transition-colors duration-300"><i class="fab fa-twitter"></i></a>
    <!-- Additional social links -->
</div>
```
To update:
1. Replace `#` with your social media profile URLs
2. Update icons by changing `fa-twitter` to appropriate [Font Awesome](https://fontawesome.com/icons) brand icons

## Adding Privacy and Terms Pages

### Footer Link Setup
Locate the footer links section:
```html
<ul class="space-y-2">
    <li><a href="#" class="hover:text-white transition-colors duration-300">Terms</a></li>
    <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy</a></li>
</ul>
```

To link privacy and terms pages:
1. Create `privacy.html` and `terms.html` in your root directory
2. Update the href attributes:
```html
<li><a href="./terms.html" class="hover:text-white transition-colors duration-300">Terms</a></li>
<li><a href="./privacy.html" class="hover:text-white transition-colors duration-300">Privacy</a></li>
```

## Troubleshooting

### Common Issues:

1. **Broken Links**
   - Check for typos in `href` attributes
   - Verify file paths are correct
   - Ensure linked files exist in the specified location

2. **Styling Problems**
   - Check Tailwind CSS classes for typos
   - Maintain responsive classes (e.g., `md:text-2xl`)
   - Keep paired classes together (e.g., `hover:` effects)

3. **Icons Not Showing**
   - Verify Font Awesome CDN link is present in `<head>`
   - Check icon class names against Font Awesome documentation
   - Ensure proper icon prefix (`fas`, `fab`, etc.)

### Need Help?
If you encounter issues:
1. Validate your HTML at [W3C Validator](https://validator.w3.org/)
2. Check the browser console for errors (F12)
3. Review Tailwind CSS documentation for correct class usage

Remember to always test changes in multiple browsers and screen sizes before deploying to production.