# Portfolio Website

A modern, responsive portfolio website inspired by professional design trends. This portfolio features a clean, minimalist design with smooth animations and interactive elements.

## Features

- **Responsive Design**: Fully responsive layout that works on all devices
- **Modern UI/UX**: Clean, professional design with smooth animations
- **Interactive Elements**: 
  - Smooth scrolling navigation
  - Portfolio filtering system
  - Contact form with validation
  - Scroll-triggered animations
  - Typing animation for hero section
- **Performance Optimized**: Lightweight and fast-loading
- **Accessibility**: Semantic HTML and keyboard navigation support

## Sections

1. **Hero Section**: Eye-catching introduction with call-to-action buttons
2. **About Section**: Personal information, skills, and statistics
3. **Portfolio Section**: Filterable project showcase
4. **Contact Section**: Contact form and information
5. **Footer**: Social links and copyright information

## Technologies Used

- **HTML5**: Semantic markup
- **CSS3**: Modern styling with Flexbox and Grid
- **JavaScript**: Interactive functionality and animations
- **Font Awesome**: Icons
- **Google Fonts**: Inter font family

## Customization Guide

### Personal Information
Update the following in `index.html`:

1. **Name and Title**:
   ```html
   <title>Your Name - Portfolio</title>
   <h1 class="hero-title">Hi, I'm <span class="highlight">Your Name</span></h1>
   <h2 class="hero-subtitle">Your Professional Title</h2>
   ```

2. **About Section**:
   - Update the description in the about section
   - Modify skills in the skills grid
   - Update statistics in the stats section

3. **Portfolio Projects**:
   - Replace placeholder projects with your actual work
   - Update project titles, descriptions, and links
   - Add real project images

4. **Contact Information**:
   - Update email, phone, and location
   - Add your social media links

### Styling Customization

1. **Colors**: Modify the CSS custom properties in `styles.css`:
   ```css
   :root {
     --primary-color: #007bff;
     --secondary-color: #ffd700;
     --text-color: #333;
     --bg-color: #fff;
   }
   ```

2. **Fonts**: Change the Google Fonts import and font-family declarations

3. **Layout**: Adjust grid layouts and spacing as needed

### Adding Real Images

Replace the placeholder divs with actual images:

```html
<!-- Replace this -->
<div class="image-placeholder">
    <i class="fas fa-user"></i>
</div>

<!-- With this -->
<img src="path/to/your/image.jpg" alt="Your Name" class="hero-image">
```

## File Structure

```
portfolio-25/
├── index.html          # Main HTML file
├── styles.css          # CSS styles
├── script.js           # JavaScript functionality
└── README.md           # This file
```

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers

## Performance Features

- Optimized images and assets
- Minimal JavaScript for fast loading
- CSS animations using transform and opacity
- Lazy loading for better performance

## Deployment

### GitHub Pages
1. Push your code to a GitHub repository
2. Go to repository Settings > Pages
3. Select source branch (usually `main`)
4. Your site will be available at `https://username.github.io/repository-name`

### Netlify
1. Drag and drop your project folder to Netlify
2. Or connect your GitHub repository for automatic deployments

### Vercel
1. Import your GitHub repository
2. Deploy with zero configuration

## Contact Form Setup (EmailJS)

The contact form is now integrated with EmailJS for real email functionality. Follow these steps to set it up:

### 1. Create EmailJS Account
1. Go to [EmailJS.com](https://www.emailjs.com/)
2. Sign up for a free account
3. Verify your email address

### 2. Set Up Email Service
1. In your EmailJS dashboard, go to **Email Services**
2. Click **Add New Service**
3. Choose your email provider (Gmail, Outlook, etc.)
4. Follow the setup instructions for your provider
5. Note down your **Service ID**

### 3. Create Email Template
1. Go to **Email Templates** in your dashboard
2. Click **Create New Template**
3. Use this template content:

```
Subject: New Contact Form Message - {{subject}}

From: {{from_name}}
Email: {{from_email}}
Subject: {{subject}}

Message:
{{message}}

---
This message was sent from your portfolio contact form.
```

4. Note down your **Template ID**

### 4. Get Public Key
1. Go to **Account** > **General**
2. Copy your **Public Key**

### 5. Update Configuration
In `script.js`, replace these values with your actual credentials:

```javascript
const EMAILJS_SERVICE_ID = 'your_service_id_here';
const EMAILJS_TEMPLATE_ID = 'your_template_id_here';
const EMAILJS_PUBLIC_KEY = 'your_public_key_here';
```

### 6. Update Recipient Email
In the contact form handler, replace:
```javascript
to_email: 'your.email@example.com' // Replace with your actual email
```

### 7. Test the Form
1. Open your website
2. Fill out the contact form
3. Submit and check if you receive the email

### Alternative Email Services

If you prefer other services:

- **Formspree**: Simple form handling
- **Netlify Forms**: If hosting on Netlify
- **Custom Backend**: Node.js/Express with Nodemailer

## SEO Optimization

- Semantic HTML structure
- Meta tags for social sharing
- Alt text for images
- Clean URL structure
- Fast loading times

## Future Enhancements

- [ ] Blog section
- [ ] Dark mode toggle
- [ ] Multi-language support
- [ ] Advanced animations
- [ ] CMS integration
- [ ] Analytics integration

## License

This project is open source and available under the [MIT License](LICENSE).

## Support

If you have any questions or need help customizing this portfolio, feel free to reach out!

---

**Note**: Remember to replace all placeholder content with your actual information before deploying your portfolio.
