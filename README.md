# Texas Web Design Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Texas Web Design landing page. Written for beginners, it covers essential modifications while preserving the page's responsive design and functionality.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the company logo and navigation menu:
```html
<div class="text-2xl font-bold text-blue-600">TWD</div>
```
To modify:
- Change "TWD" to your company name
- Adjust size using `text-2xl` (options: text-sm, text-base, text-lg, text-2xl, text-3xl)
- Modify color using `text-blue-600` (options: text-[color]-[shade])

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">Texas Web Design</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">Best Websites In Texas</p>
```
To modify:
- Update heading and subheading text
- Adjust responsive text sizes:
  - Mobile: `text-4xl`
  - Tablet: `md:text-5xl`
  - Desktop: `lg:text-6xl`

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white rounded-2xl p-8 shadow-lg hover:shadow-xl transition-shadow duration-300">
    <h3 class="text-xl font-semibold mb-4">Feature Title</h3>
    <p class="text-gray-600">Feature description text.</p>
</div>
```
To modify:
- Update feature titles and descriptions
- Adjust padding using `p-8` (options: p-2, p-4, p-6, p-8)
- Modify shadow using `shadow-lg` (options: shadow-sm, shadow, shadow-lg, shadow-xl)

## Fixing Broken Links

### Navigation Menu Links
Current navigation links:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```
To update:
1. Identify the section ID you want to link to
2. Update the `href` attribute with `#section-id`
3. Example: `<a href="#new-section">New Section</a>`

### External Links
Current external links:
```html
<a href="https://twd.com" class="inline-block px-8 py-4 bg-blue-600">Start Your Project</a>
```
To update:
1. Replace `https://twd.com` with your website URL
2. Ensure URLs include `https://` prefix
3. Test links after updating

## Linking Privacy and Terms Pages

### Footer Legal Links
Current placeholder links:
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```
To add proper links:
1. Create privacy.html and terms.html files
2. Update href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Check that section IDs match href attributes
   - Ensure IDs are unique
   - Example: `<section id="features">` matches `<a href="#features">`

2. **Responsive Design Issues**
   - Verify mobile-first classes are present
   - Check breakpoint prefixes (sm:, md:, lg:)
   - Example: `text-4xl md:text-5xl lg:text-6xl`

3. **Styling Inconsistencies**
   - Maintain consistent color classes (e.g., text-blue-600)
   - Use provided spacing scale (mb-4, mb-6, mb-8, etc.)
   - Keep consistent padding/margin patterns

### Best Practices
- Always test changes on multiple screen sizes
- Maintain accessibility by keeping sufficient color contrast
- Preserve responsive design classes when updating
- Back up files before making changes
- Test all links after updating

For additional help or specific customizations, refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs) or contact your web development team.