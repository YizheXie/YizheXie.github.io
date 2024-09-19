# Easy-to-use Personal Academic Homepage Template

**Special Thanks**: This template was modified from Tengyu Ma's and Danqi Chen's.

## 00 Background

GitHub provides each user with a subdomain `<user-id>.github.io`, and users can easily create their own homepage by setting up a repository named `<user-id>.github.io` and pushing static pages to the `master` branch. The homepage should be named `index.html`.

## 01 Creating the Repository

**Note**: The repository name must be in the format `username.github.io`.

For example, my repository is named `YizheXie.github.io`. After creating the repository, if it contains no content, the site will not be hosted. You can either create an empty `index.html` file or clone my repository content into your `master` branch. Then, go to the repository's `Settings` page, find `Pages` in the left sidebar, and check if it displays the message: `"Your site is live at https://xxxxxxx.github.io/"`. If you see this, your site is successfully created, and you can start customizing your homepage.

## 02 Customizing the Homepage

You can choose any HTML template you like, or you can directly use mine. Next, I will provide a step-by-step guide on how to modify my template.

### 1. Customizing the `<head>` Section

The `<head>` section in an HTML file defines the document's metadata, styles, and scripts. This section typically includes the page title, character encoding, stylesheets, scripts, and SEO-related tags. 

You can modify this part to better optimize your personal homepage, Locate the section:

```html
<head>
    <title>Yizhe Xie's Homepage</title>
    <meta http-equiv="Content-Type" content="text/html; charset=UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta name="author" content="Yizhe Xie">
    <meta name="keywords" content="Yizhe Xie, Yizhe Xie MUC, Yizhe Xie Artificial Intelligence">
    <meta name="robots" content="index,follow">
    <meta name="description" content="Homepage of Yizhe Xie">
    <link href="https://fonts.googleapis.com/css?family=Lato:100,300,400,700,900" rel="stylesheet">
    <link rel="stylesheet" type="text/css" media="screen,print" href="css/style.css" />
    <link href="css/bootstrap.min.css" rel="stylesheet" media="screen" />
    <link rel="icon" type="image/png" href="./images/logos/github.png">
    <script type="text/javascript" src="https://me.kis.v2.scr.kaspersky-labs.com/FD126C42-EBFA-4E12-B309-BB3FDD723AC1/main.js" charset="UTF-8"></script>
    <style>
      .button {
        background-color: #e7e7e7; color: black;
        border: none;
        text-decoration: none;
        display: inline-block;
        margin: 4px 2px;
        cursor: pointer;
      }
    </style>
</head>
```

First, you can modify the `<title>` tag by replacing it with your own name or the title of your homepage. For example, change `Yizhe Xie's Homepage` to `[Your Name]'s Homepage`. Next, for the `<meta>` tags, which contain metadata for the page, you can update the `author`, `description`, and `keywords` based on your content. Replace `Yizhe Xie` with your own name, update `Homepage of Yizhe Xie` with a short description of your homepage, and adjust the `keywords` to reflect the main topics of your site.

For fonts and styles, you can keep the Google font `Lato` or replace it with a font of your choice. In the stylesheet links, you can customize or replace `style.css` and `Bootstrap` files as needed. After that, you can update the icon path in the `<link rel="icon">` tag with your own favicon file. Finally, if there are external scripts you don’t need, you can remove them or replace them with other JavaScript files you want to load.

### 2. Modify Personal Information

Locate the section containing personal information such as name, email, and university:

```html
<h1>
    Yizhe Xie
    <span style="font-family: STFangsong; font-size: 20pt; position: relative; top: -4px;">
      (谢奕哲)
    </span>
</h1>  
<p style="font-size: 18px;">
   <strong>Undergraduate</strong><br>
   Minzu University of China & City University of Macau<br>
   <b>Email</b>: 23160151@muc.edu.cn<br>
   <b>Or</b>: D23090600701@cityu.edu.mo<br>
   <a href="https://github.com/YizheXie" target="_blank">Github</a>
</p>
```

You can replace the name, email, and GitHub link with your own information. Keep the text styles consistent to maintain uniformity across the page. Here, I choose `font-size: 18px`.

### 3. Add a Personal Photo

Replace the default photo with your own by updating the `src="images/selfie1.jpg"` path to your own image file:

```html
<img class="img-responsive" style="max-height:400px;" src="images/selfie1.jpg"/>
```

Ensure the image size does not exceed 400px to avoid layout issues.

### 4. Customize Research Interests

Update the "About" section to reflect your research interests:

```html
<p style="font-size: 18px;">
    Hello! I am a second-year undergraduate pursuing a double degree in Data Science and Big Data Technology at Minzu University of China and City University of Macau. I am fortunate to be advised by <a href="https://fds.cityu.edu.mo/members/341">Congcong Zhu</a> at CityU of Macau. My research interests include large language model (LLM) safety, multi-agents learning, especially LLM-MA and (deep) reinforcement learning.
</p>
```

Modify this section to describe your current research, your advisor, and the projects you are involved in.

### 5. Update Publication List

In the `Publications` section, you can add or update your papers. Locate the following code and update it:

```html
<ul id="manuscript" style="display:none;"></ul>

<h4>
  <button class="button" onclick="myFunction('conference')">
  Conference Papers 
  </button>
</h4>
<ul id="conference" style="display:none;">
</ul>
```

Use the addpaper() function to add your new paper to the respective list:

```html
addpaper("#",
         "Your Paper Title",
         "Your Name, Co-author Name",
         "Conference Name",
         "Conference Level",
         "Year",
         "Bibtex string",
         "unique_paper_id", 
         'conference',
         null,
         null, 
         null);
```

### 6. Customize Project Showcase

In the `Programs & Column` section, you can showcase your projects. Add your project link and description to the list:

```HTML
<ul>
    <li>My Custom Project. <a href="your_project_link">Link</a></li>
</ul>
```

### 7. Update Research Group Information

Finally, update the "Research Group" section with your own research team information. Here's a snippet from the template:

```HTML
<p style="font-size: 18px;">
    Our research focuses include Computer Vision, Medical imaging and LLM safety. Our team leader, <b>Dongxiao Li</b>, is a docile, bright and generous person. If you are interested in joining our group for collaborative learning and growth, please feel free to reach out to him.
</p>
```

You can modify the research focus, team members, and contact details.

### 03 Publishing and Updating the Homepage

After completing your homepage customization, remember to commit your changes to the `master` branch and push them to GitHub. Your page will automatically update in a few minutes. Visit `https://<your-username>.github.io` to see the latest version.