# Featured Projects - Image Slider Setup Guide

## Overview

The featured projects slider on your website now dynamically loads images and captions from the `global_config.json` file. This makes it easy to update your featured projects without editing the HTML code.

## Folder Structure

```
your-website/
├── index.html
├── global_config.json
├── featured_projects_images/
│   ├── project1.jpg
│   ├── project2.jpg
│   ├── project3.jpg
│   ├── project4.jpg
│   └── project5.jpg
└── logo/
    └── logo_9.svg
```

## How to Add/Update Featured Projects

### Step 1: Add Your Images

1. Place your project images in the `featured_projects_images` folder
2. Recommended image specifications:
   - **Resolution**: 1200px × 500px (or similar aspect ratio)
   - **Format**: JPG, PNG, or WebP
   - **File size**: Optimize images to under 500KB for faster loading
   - **Naming**: Use descriptive names like `waterproofing_terrace.jpg`, `modular_kitchen_modern.jpg`

### Step 2: Update global_config.json

Open `global_config.json` and find the `featuredProjects` section. Each project has the following structure:

```json
{
  "id": 1,
  "image": "featured_projects_images/project1.jpg",
  "caption": "Expert Waterproofing Solutions - 10+ Years Leak-Free Guarantee",
  "category": "waterproofing",
  "altText": "Waterproofing Solutions"
}
```

**Field Descriptions:**

- `id`: Unique identifier for the project (sequential number)
- `image`: Path to the image file (relative to index.html)
- `caption`: Text displayed at the bottom of the slide
- `category`: Project category (waterproofing, interior, metal, painting, upvc, renovation)
- `altText`: Alternative text for accessibility and SEO

### Step 3: Example Configuration

Here's an example with 5 featured projects:

```json
"featuredProjects": [
    {
        "id": 1,
        "image": "featured_projects_images/waterproofing_terrace.jpg",
        "caption": "Expert Waterproofing Solutions - 10+ Years Leak-Free Guarantee",
        "category": "waterproofing",
        "altText": "Terrace Waterproofing Project"
    },
    {
        "id": 2,
        "image": "featured_projects_images/modular_kitchen_lshape.jpg",
        "caption": "Transform Your Space - Custom Interior & Modular Kitchen Design",
        "category": "interior",
        "altText": "L-Shaped Modular Kitchen"
    },
    {
        "id": 3,
        "image": "featured_projects_images/metal_gate_custom.jpg",
        "caption": "Premium Metal Works - Durable, Elegant, Custom-Made",
        "category": "metal",
        "altText": "Custom Metal Gate Design"
    },
    {
        "id": 4,
        "image": "featured_projects_images/exterior_painting.jpg",
        "caption": "Professional Painting Services - Interior & Exterior Excellence",
        "category": "painting",
        "altText": "Building Exterior Painting"
    },
    {
        "id": 5,
        "image": "featured_projects_images/upvc_windows.jpg",
        "caption": "UPVC & Aluminium Solutions - Energy Efficient, Weather Resistant",
        "category": "upvc",
        "altText": "UPVC Windows Installation"
    }
]
```

## Features

### Automatic Slider

- **Auto-play**: Slides change automatically every 5 seconds
- **Navigation buttons**: Previous/Next arrows for manual control
- **Dot indicators**: Click on dots to jump to specific slides
- **Responsive**: Works perfectly on mobile, tablet, and desktop
- **Smooth transitions**: Professional slide animations

### SEO Benefits

- `altText` improves image SEO and accessibility
- `category` helps organize projects
- Lazy loading for better page performance

## Adding More Projects

To add more projects:

1. Add new image to `featured_projects_images` folder
2. Add new entry to `featuredProjects` array in `global_config.json`
3. Save the file - the slider will automatically update!

Example of adding a 6th project:

```json
{
  "id": 6,
  "image": "featured_projects_images/bathroom_renovation.jpg",
  "caption": "Complete Bathroom Renovation - Modern Fixtures & Waterproofing",
  "category": "renovation",
  "altText": "Bathroom Renovation Project"
}
```

## Removing Projects

To remove a project:

1. Delete the entry from the `featuredProjects` array in `global_config.json`
2. Optionally delete the image file from `featured_projects_images` folder

## Best Practices

### Image Guidelines

- Use high-quality, professional photos
- Ensure images are well-lit and showcase your best work
- Maintain consistent aspect ratio (1200×500 recommended)
- Compress images without losing quality (use tools like TinyPNG)

### Caption Guidelines

- Keep captions clear and concise (under 100 characters)
- Highlight the unique value or benefit
- Use action-oriented language
- Include key differentiators (warranty, quality, expertise)

### Category Guidelines

Use these standard categories:

- `waterproofing` - All waterproofing projects
- `interior` - Interior design and renovation
- `kitchen` - Modular kitchens specifically
- `metal` - Metal fabrication and works
- `painting` - Painting services
- `upvc` - UPVC and aluminium solutions
- `renovation` - General repairs and renovations

## Troubleshooting

### Images Not Showing

1. Check that image path in `global_config.json` matches actual file location
2. Verify image file names (case-sensitive on some servers)
3. Ensure images are in the correct folder (`featured_projects_images`)

### Slider Not Working

1. Clear browser cache and refresh
2. Check browser console for JavaScript errors
3. Verify `global_config.json` has valid JSON syntax (use a JSON validator)

### Slow Loading

1. Compress images to reduce file size
2. Use WebP format for better compression
3. Ensure lazy loading is enabled (already implemented)

## Technical Notes

- The slider automatically initializes after loading `global_config.json`
- Minimum 1 project required, no maximum limit
- Images load with lazy loading for better performance
- Slider maintains state when navigating within the page
- Mobile-responsive with touch-friendly controls

## Support

For technical issues or questions, contact the development team or refer to the main website documentation.

---

**Last Updated**: January 2025
**Version**: 1.0
