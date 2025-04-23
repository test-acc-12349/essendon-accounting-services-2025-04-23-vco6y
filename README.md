# Essendon Accounting Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Essendon Accounting landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name:**
```html
<!-- Find this section in the header -->
<div class="text-2xl font-bold text-white">
    <a href="/" class="flex items-center space-x-2">
        <i class="fas fa-calculator text-blue-500"></i>
        <span>Essendon Accounting</span> <!-- Change text here -->
    </a>
</div>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#services" class="text-gray-300 hover:text-white transition-colors duration-300">Services</a> <!-- Edit menu text here -->
</div>
```

### Hero Section
The main banner section contains your primary headline and call-to-action:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-clip-text text-transparent bg-gradient-to-r from-blue-400 to-blue-600">
    Essendon accounting services <!-- Update main headline here -->
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12 leading-relaxed">
    Trusted advisors for your financial future <!-- Update subheading here -->
</p>
```

### Tailwind CSS Classes Explained
- `text-4xl`: Sets font size (increases with screen size)
- `md:text-5xl`: Applies different font size on medium screens
- `mb-8`: Adds margin bottom spacing
- `bg-gray-900`: Sets background color
- `text-gray-300`: Sets text color
- `hover:text-white`: Changes text color on hover

## Fixing Broken Links

### Current Link Inventory
1. Navigation Menu Links:
```html
<a href="#services">Services</a>
<a href="#benefits">Benefits</a>
<a href="#contact">Contact</a>
<a href="https://theaccountants.com">Get Started</a> <!-- Update with actual URL -->
```

### Updating Links Step-by-Step:
1. Internal Links (Sections):
   - Keep the `#` symbol for same-page navigation
   - Ensure the ID matches in the corresponding section
   ```html
   <!-- Navigation link -->
   <a href="#services">Services</a>

   <!-- Corresponding section -->
   <section id="services" class="py-24 bg-gray-800">
   ```

2. External Links:
   - Replace placeholder URLs with actual destinations
   ```html
   <!-- Find this in the hero section -->
   <a href="https://theaccountants.com" class="inline-block bg-blue-600...">
   <!-- Replace with your actual URL -->
   ```

## Linking Privacy and Terms Pages

### Footer Links Setup
1. Locate the footer legal section:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

2. Update the href attributes:
```html
<!-- Replace # with actual file paths -->
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Check that section IDs match exactly with href values
   - IDs are case-sensitive
   ```html
   <!-- These must match exactly -->
   <a href="#services">
   <section id="services">
   ```

2. **Responsive Design Issues**
   - Ensure you maintain the responsive classes when editing
   - Key responsive prefixes: `sm:`, `md:`, `lg:`
   ```html
   <!-- Example of responsive classes -->
   <h1 class="text-4xl md:text-5xl lg:text-6xl">
   ```

3. **Icon Display Problems**
   - Verify Font Awesome is properly loaded
   - Check icon class names match exactly
   ```html
   <i class="fas fa-calculator text-blue-500"></i>
   ```

### Best Practices
- Always test changes across different screen sizes
- Maintain consistent spacing using Tailwind's spacing classes
- Keep the color scheme consistent using existing color classes
- Back up files before making major changes

Need further assistance? Contact technical support or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).