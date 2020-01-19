# Rails 6 + webpack + Bootstrap 4 Datetime Picker 

* Ruby version : 2.6.5
* Rails version : 6.0.2.1

#### yarn add jquery popper.js moment
config/webpack/environments.js
<pre><code>const { environment } = require('@rails/webpacker')
const webpack = require('webpack')
environment.plugins.prepend(
    'Provide',
    new webpack.ProvidePlugin({
        $: 'jquery/src/jquery',
        jQuery: 'jquery/src/jquery',
        jquery: 'jquery/src/jquery',
        Popper: 'popper.js/dist/popper',
        moment: 'moment/moment'
    })
)
module.exports = environment</code></pre>

#### yarn add bootstrap 
#### yarn add tempusdominus-bootstrap-4
app/javascript/application.js
<pre><code>require("moment/locale/ja")
require("tempusdominus-bootstrap-4")
import '../stylesheets/application'
</code></pre>

app/javascript/stylesheets/application.scss
<pre><code>@import "~bootstrap/scss/bootstrap";
@import "~tempusdominus-bootstrap-4/src/sass/tempusdominus-bootstrap-4";
</code></pre>

#### Check in browser console
<pre><code>$.fn.jquery;
$('.datetimepicker').datetimepicker();
</code></pre>

https://tempusdominus.github.io/bootstrap-4/
