# HTML-Standards
A list of HTML coding standards I will use. This will be updated over time and will be used in future projects, and current projects created before these standards will be updated to match these.

## Page Structure
Each page will be structured with a seperate `<header>` and `<body>` tag that will be used to seperate out the page header from the rest of the page. For more about page headers please see the Page Header section.

When using Bootstrap, all body content will also be inside a `.container` or `.container-fluid`. This can have further `.container`s or `.container-fluid`s, depending on the needs of the page.

## Page Header
Every navbar inside a `<header>` will have the classes `.container` or `.container-fluid` and will generally look like the following (written with BS5):
```html
<header>
    <div class="container-fluid">
        <nav class="navbar navbar-expand-md navbar-dark fixed-top bg-dark">
            <a class="navbar-brand" href="#">Site Brand</a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarCollapse" aria-controls="navbarCollapse" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div id="navbarCollapse" class="navbar-collapse collapse">
                <ul class="nav navbar-nav bg-dark">
                    <li class="nav-item"><a class="nav-link active" href="#">Current Page</a></li>
                    <li class="nav-item"><a class="nav-link" href="page2.html">New Page</a></li>
                </ul>
            </div>
        </nav>
    </div>
</header>
```

## .htaccess Page Name Rewrites
Generally the following rules will be applied for `.htaccess` page name rewrites. Just replace the domain names with the correct ones.
```
<IfModule mod_rewrite.c> 
Options +FollowSymLinks -MultiViews

RewriteEngine On 
RewriteBase /

#www to non
RewriteCond %{HTTP_HOST} ^www\.(([a-z0-9_]+\.)?katiethe\.dev)$ [NC]
RewriteRule ^(.+?)/?$ http://%1/$1/ [R=301,L]

#html
RewriteCond %{REQUEST_FILENAME} !-f 
RewriteCond %{REQUEST_FILENAME} !-d 
RewriteRule ^([^\.]+)$ $1.html [NC,L]

#index redirect 
RewriteCond %{THE_REQUEST} ^[A-Z]{3,9}\ /index\.html\ HTTP/ 
RewriteRule ^index\.html$ https://katiethe.dev/ [R=301,L]
RewriteCond %{THE_REQUEST} \.html 
RewriteRule ^(.*)\.html$ /$1 [R=301,L]
</IfModule>
```

## JavaScript
I will be following most JavaScript conventions normally.

## Tab Spacing
I will always use a standard tab width (4 spaces) when writing HTML.

## Space within tags and new lines
There will be no space between any `<p>` tag and the content inside of it. Any paragraph will be single-line, but new tags will always be a new line.
