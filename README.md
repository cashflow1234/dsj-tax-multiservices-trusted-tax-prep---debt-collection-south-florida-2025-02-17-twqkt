# DSJ Tax Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the DSJ Tax landing page. Follow these steps carefully to make updates while preserving the page's functionality and design.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the company logo and navigation menu:

```html
<div class="text-2xl font-bold text-blue-500">DSJ Tax</div>
```

To update the company name:
1. Locate this div in the header section
2. Replace "DSJ Tax" with your desired text
3. Adjust text size using Tailwind classes:
   - `text-xl` (smaller)
   - `text-2xl` (current size)
   - `text-3xl` (larger)

### Hero Section Text
To update the main headline:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8">
    Reliable Tax Prep & Debt Collection
    <span class="block text-blue-500">We've Got You Covered</span>
</h1>
```

Customize by:
1. Changing the main text ("Reliable Tax Prep & Debt Collection")
2. Modifying the blue tagline ("We've Got You Covered")
3. Adjusting responsive text sizes:
   - `text-4xl`: mobile devices
   - `md:text-5xl`: medium screens
   - `lg:text-6xl`: large screens

### Features Section
Each feature card follows this structure:

```html
<div class="bg-gray-900 p-8 rounded-2xl hover:transform hover:scale-105 transition-all duration-300">
    <div class="w-16 h-16 bg-blue-600 rounded-full flex items-center justify-center mb-6">
        <i class="fas fa-shield-alt text-2xl"></i>
    </div>
    <h3 class="text-xl font-semibold mb-4">Trust</h3>
    <p class="text-gray-400">Built on years of experience and customer satisfaction</p>
</div>
```

To modify:
1. Change the icon by updating the `fas fa-shield-alt` class to any [Font Awesome icon](https://fontawesome.com/icons)
2. Update the heading text ("Trust")
3. Modify the description text
4. Adjust spacing using `mb-` classes (margin-bottom)

## Fixing Broken Links

### Navigation Menu Links
Current navigation links:

```html
<div class="hidden md:flex space-x-8">
    <a href="#services" class="hover:text-blue-400 transition-colors duration-300">Services</a>
    <a href="#benefits" class="hover:text-blue-400 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="hover:text-blue-400 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="hover:text-blue-400 transition-colors duration-300">Contact</a>
</div>
```

To update:
1. Locate the section ID you want to link to (e.g., `id="benefits"`)
2. Ensure the `href` attribute matches exactly (e.g., `href="#benefits"`)
3. For external links, replace with full URL (e.g., `href="https://example.com"`)

### Get Started Button
Current implementation:

```html
<a href="https://form.jotform.com/250476421727054" class="bg-blue-600 hover:bg-blue-700 px-6 py-2 rounded-full">
    Get Started
</a>
```

To update:
1. Replace the JotForm URL with your form's URL
2. Test the link to ensure it opens the correct form
3. Maintain the class attributes for consistent styling

## Linking Privacy and Terms Pages

### Footer Links Section
Current implementation:

```html
<div>
    <h4 class="text-lg font-semibold mb-6">Legal</h4>
    <ul class="space-y-4 text-gray-400">
        <li><a href="#" class="hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-blue-400 transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Create privacy.html and terms.html files in your project directory
2. Update the href attributes:

```html
<li><a href="privacy.html" class="hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-blue-400 transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

Common issues and solutions:

1. **Broken Internal Links**
   - Ensure section IDs match href attributes exactly
   - IDs are case-sensitive
   - Check for extra spaces in IDs

2. **Responsive Design Issues**
   - Verify Tailwind responsive prefixes:
     - `md:` for medium screens
     - `lg:` for large screens
   - Test on multiple devices

3. **Icon Not Displaying**
   - Confirm Font Awesome CDN is properly loaded
   - Check icon class names against Font Awesome documentation
   - Ensure internet connectivity for CDN access

4. **Style Changes Not Applying**
   - Verify Tailwind CDN is properly loaded
   - Check for typos in class names
   - Ensure classes are space-separated

Remember to test all changes across different devices and browsers before deploying to production.