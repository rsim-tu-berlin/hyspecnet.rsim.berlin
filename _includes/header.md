<!DOCTYPE html>
<!--[if lt IE 7]>      <html class="no-js lt-ie9 lt-ie8 lt-ie7"> <![endif]-->
<!--[if IE 7]>         <html class="no-js lt-ie9 lt-ie8"> <![endif]-->
<!--[if IE 8]>         <html class="no-js lt-ie9"> <![endif]-->
<!--[if gt IE 8]><!-->
<html class="no-js">
  <!--<![endif]-->

  <head>
    <!-- META -->
    <meta http-equiv="content-type" content="text/html; charset=UTF-8" />
    <meta name="description" content="{{ site.data.config.name }}" />
    <meta charset="UTF-8" />

    <!-- mobile responsive meta -->
    <meta name="viewport" content="width=device-width, initial-scale=1" />

    <title>{{ site.data.config.name }} - {{ site.data.config.title }}</title>
    <!-- <link rel="stylesheet" href="{{ site.baseurl }}/assets/css/style.css"> -->

    <!-- ** Plugins Needed for the Project ** -->
    <!-- Bootstrap -->
    <link
      rel="stylesheet"
      href="{{ site.baseurl }}/assets/plugins/bootstrap/css/bootstrap.min.css"
    />
    <link
      rel="stylesheet"
      href="{{ site.baseurl }}/assets/plugins/bootstrap-icons/bootstrap-icons.css"
    />
    <link
      rel="stylesheet"
      href="{{ site.baseurl }}/assets/plugins/fontawesome-6.4.0/css/all.min.css"
    />
    <link
      rel="stylesheet"
      href="{{ site.baseurl }}/assets/css/index.css"
    />

    <script src="{{ site.baseurl }}/assets/plugins/bootstrap/js/bootstrap.bundle.min.js"></script>

  </head>

  <body>
    <!-- ======= Top Bar ======= -->
    <section id="topbar" class="d-flex align-items-center">
      <div class="container d-flex justify-content-center justify-content-md-between">
        <div class="contact-info d-flex align-items-center">
        </div>
      </div>
    </section>
    <nav class="navbar navbar-expand-lg bg-light">
      <div class="container d-flex justify-content-left justify-content-md-between">
        <h1 class="logo">
          <a class="navbar-brand" href="{{ site.baseurl }}/">
          {{ site.data.config.name }}
          </a>
        </h1>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse justify-content-end" id="navbarSupportedContent">
          <ul>
          {% for menu_item in site.data.config.menu %}
            <li>
              <a
                class="nav-link scrollto"
                href="{{ site.baseurl }}{{ menu_item.link }}"
              >{{ menu_item.title }}</a>
            </li>
            {% endfor %}
          </ul>
        </div>
      </div>
    </nav>
    <section class="patches justify-items-center">
      <div class="container">
        <div class="row">
        {% for i in (1..20) %}
            <div class="col m-0 p-0">
                <img src="{{ site.url }}/../assets/images/thumbnails/{{ i }}.jpg">
            </div>
        {% endfor %}
        </div>
      </div>
    </section>
    <section class="logos">
      <div class="container">
        <div class="row">
            <div class="col">
                <div class="text-center mx-auto mb-5 mb-lg-0 mb-lg-3">
                    <a href="https://www.tu-berlin.de" target="_blank">
                        <img src="{{ site.url }}/assets/images/tu-logo.svg" class="img-responsive center-block" style="height: 50px">
                    </a>
                </div>
            </div>
            <div class="col">
                <div class="text-center mx-auto mb-5 mb-lg-0 mb-lg-3">
                    <a href="http://bifold.berlin" target="_blank">
                        <img src="{{ site.url }}/assets/images/BIFOLD.svg" class="img-responsive center-block" style="height: 50px">
                    </a>
                </div>
            </div>
            <div class="col">
                <div class="text-center mx-auto mb-5 mb-lg-0 mb-lg-3">
                    <a href="https://rsim.berlin" target="_blank">
                        <img src="{{ site.url }}/assets/images/rsim-logo.png" class="img-responsive center-block" style="height: 50px">
                    </a>
                </div>
            </div>
            <div class="col">
                <div class="text-center mx-auto mb-5 mb-lg-0 mb-lg-3">
                    <a href="http://www.bigearth.eu" target="_blank">
                        <img src="{{ site.url }}/assets/images/BigEarth.png" class="img-responsive center-block" style="height: 50px">
                    </a>
                </div>
            </div>
        </div>
      </div>
    </section>
