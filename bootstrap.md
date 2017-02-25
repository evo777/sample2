Bootstrap is an HTML, CSS and Javascript framework for developing responsive, mobile-first web applications.

## Setup

### Bootstrap CDN
    <!-- Latest compiled and minified CSS -->
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/css/bootstrap.min.css"    integrity="sha384-1q8mTJOASx8j1Au+a5WDVnPi2lkFfwwEAa8hDDdjZlpLegxhjVME1fgjWPGmkzs7" crossorigin="anonymous">

    <!-- Latest compiled and minified JavaScript -->
    <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/js/bootstrap.min.js" integrity="sha384-0mSbJDEHialfmuBBQP6A4Qrprq5OVfW37PRR3j5ELqxss1yVqOtnepnHVP9aJ7xS" crossorigin="anonymous"></script>

### Install with Bower
    bower install bootstrap

### Install with npm
    npm install bootstrap

### Basic Template
    <!DOCTYPE html>
    <html lang="en">
        <head>
        <meta charset="utf-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <title>Bootstrap 101 Template</title>

        <!-- Bootstrap -->
        <link href="css/bootstrap.min.css" rel="stylesheet">

        <script src="https://oss.maxcdn.com/html5shiv/3.7.2/html5shiv.min.js"></script>
        <script src="https://oss.maxcdn.com/respond/1.4.2/respond.min.js"></script>
      </head>
      <body>
        <h1>Hello, world!</h1>
        <!-- jQuery (necessary for Bootstrap's JavaScript plugins) -->
        <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.3/jquery.min.js"></script>

        <!-- Include all compiled plugins (below), or include individual files as needed -->
        <script src="js/bootstrap.min.js"></script>
      </body>
    </html>

## Grid System
Bootstrap includes a responsive, fluid grid system that scales up to 12 columns as the viewport size increases. Grid systems are used for creating page layouts with rows and columns to structure your content.

Rows are placed within either a .container or .container-fluid class.

Rows are used to create horizontal groups of columns.

Content goes within columns, and only columns can be immediate children of rows.

You can indicate how many columns you want a given column to span (e.g. .col-md-4). For example, three columns that span the entire viewport would use three .col-xs-4.

Grid classes (.col-xs-, .col-sm-, .col-md-, .col-lg-) apply to screen widths greater than or equal to breakpoint sizes and override grid classes targeted at smaller devices.

### Example

    <div class="container-fluid">
        <div class="row">
            <div class="col-xs-6 col-md-4">...</div>
            <div class="col-xs-6 col-md-4">...</div>
            <div class="col-xs-6 col-md-4">...</div>
        </div>
    </div>
