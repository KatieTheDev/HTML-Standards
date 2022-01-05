# HTML-Standards
A list of HTML coding standards I will use. This will be updated over time and will be used in future projects, and current projects created before these standards will be updated to match these.

## Page Structure
Each page will be structured with a seperate `<header>` and `<body>` tag that will be used to seperate out the page header from the rest of the page. For more about page headers please see the Page Header section.

When using Bootstrap, all body content will also be inside a `.container` or `.container-fluid`. This can have further `.container`s or `.container-fluid`s, depending on the needs of the page.

## Page Header
Every navbar inside a `<header>` will have the classes `.container` or `.container-fluid` and will generally look like the following:
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
