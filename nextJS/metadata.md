## [Detailed resource to learn more about metadata in next Js ](htps://nextjs.org/learn/dashboard-app/adding-metadata)

### Most important type of metadata that matters the most are -->
### 1)title --> 
```HTML
<title>Page Title</title>
```
### 2)description->
```HTML
<meta name="description" content="A brief description of the page content." />
```
### 3)Keyword-->

```HTML
<meta name="keywords" content="keyword1, keyword2, keyword3" />
```

#### 4)Open Graph-->While the above three types of seo are made for the bots and uses html open graph utilises facebook open graph tech.What makes it different is the fact that it will be appplied when you will share content on different platforms (Eg-If you share your site link in twitter or linkedin instead of your site url your title that you want to display(Eg-your business name) will appear)

```HTML
<meta property="og:title" content="Title Here" />
<meta property="og:description" content="Description Here" />
<meta property="og:image" content="image_url_here" />
```

#### 5)Favicon --> displays the logo of your website 
'''HTML
<link rel="icon" href="path/to/favicon.ico" />
```

## Adding custom titles to specific pages
```jsx
import { Metadata } from 'next';
 
export const metadata: Metadata = {
  title: {
    template: '%s | Acme Dashboard',
    default: 'Acme Dashboard',
  },
  description: 'Xyz'
};
```
### And now to make the name of the page appear in the title (in place of %s) write the following code in the page whose name you want to add in the title 
```jsx
export const metadata: Metadata = {
  title: 'Name of your page ',
};
```
## Now when user enters this page in your website the title will become Name of your page || Xyz