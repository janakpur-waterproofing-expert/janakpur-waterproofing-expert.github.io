# Quick Start Guide - Featured Projects Update

## What Changed?

✅ Featured projects slider now loads from `global_config.json`
✅ Easy to update without touching HTML code
✅ Images stored in `featured_projects_images` folder
✅ All project data centralized in one JSON file

## Quick Update Steps

### To Update Featured Projects:

1. **Add/Replace Images**

   - Put your images in `featured_projects_images/` folder
   - Name them descriptively (e.g., `waterproofing_project_jan2025.jpg`)
   - Recommended size: 1200×500px

2. **Edit global_config.json**
   - Open `global_config.json` in any text editor
   - Find the `"featuredProjects"` section
   - Update the entries:

```json
"featuredProjects": [
    {
        "id": 1,
        "image": "featured_projects_images/your_image.jpg",
        "caption": "Your Caption Here",
        "category": "waterproofing",
        "altText": "Image Description"
    }
]
```

3. **Save & Test**
   - Save the JSON file
   - Refresh your website
   - The slider will automatically update!

## Example: Adding a New Project

Let's say you completed a new terrace waterproofing project:

**Step 1**: Add image to folder

```
featured_projects_images/terrace_waterproofing_dec2024.jpg
```

**Step 2**: Add to global_config.json

```json
{
  "id": 6,
  "image": "featured_projects_images/terrace_waterproofing_dec2024.jpg",
  "caption": "Terrace Waterproofing - 10 Year Warranty, Zero Leakage Guarantee",
  "category": "waterproofing",
  "altText": "Completed terrace waterproofing project"
}
```

**Step 3**: Done! Your new project appears in the slider.

## Categories Available

- `waterproofing` - Waterproofing projects
- `interior` - Interior design
- `kitchen` - Modular kitchens
- `metal` - Metal fabrication
- `painting` - Painting services
- `upvc` - UPVC/Aluminium works
- `renovation` - Repairs & renovation

## Tips for Great Captions

✅ DO:

- "Complete Bathroom Waterproofing - 5 Year Leak-Free Guarantee"
- "Modern L-Shaped Kitchen - Premium Fittings & Custom Design"
- "Exterior Building Painting - Weather-Resistant Professional Finish"

❌ DON'T:

- "Project 1"
- "Nice kitchen"
- "Good work"

## Common Issues

### Problem: Image doesn't show

**Solution**: Check the image path matches exactly (case-sensitive!)

### Problem: Slider not updating

**Solution**: Clear browser cache (Ctrl+Shift+R or Cmd+Shift+R)

### Problem: JSON error

**Solution**: Validate your JSON at https://jsonlint.com

## Need More Help?

See the detailed `FEATURED_PROJECTS_README.md` for:

- Complete documentation
- Image optimization tips
- Troubleshooting guide
- Best practices

---

**Remember**: You now have full control over your featured projects through `global_config.json` - no HTML coding required!
