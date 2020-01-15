# sage_customisations
Roots/Sage Customisations

Add Hamburgers menu: 
```
yarn add hamburgers
```
Add following to common.js:
```export default {
  init() {
    // JavaScript to be fired on all pages
    $('.hamburger').click(function() {
      $(this).toggleClass('is-active');
    });
  },
  finalize() {
     // JavaScript to be fired on all pages, after page specific JS is fired
  },
};
```
Then follow class names and styling info here - https://jonsuh.com/hamburgers/



Add rfs responsive text resizing:
```
yarn add rfs
```

Add animate.css (jquery might be better option if complex animations required but this is more lightweight:
```
yarn add animate.css
```

Add fontawesome the right way:
Load the core files:
```
yarn add fortawesome/fontawesome-svg-core
```
Load whichever library of icons you want/all of them:
```
yarn add @fortawesome/free-solid-svg-icons
yarn add @fortawesome/free-regular-svg-icons
yarn add @fortawesome/free-brands-svg-icons
```

In main.js:
// import then needed Font Awesome functionality
```
import { library, dom } from '@fortawesome/fontawesome-svg-core';
```
// import the Facebook and Twitter icons
```
import { faFacebook, faTwitter } from '@fortawesome/free-brands-svg-icons';
```

// add the imported icons to the library
```
library.add(faFacebook, faTwitter);
```

// tell FontAwesome to watch the DOM and add the SVGs when it detects icon markup
```
dom.watch();
```


Lightweight facebook and liknedin share button on any post:

```
<a href="https://www.facebook.com/sharer.php?u={{ get_permalink() }}" target="_blank" style="color: #636363;"><i class="fab fa-facebook"></i></a>

<a href="https://www.linkedin.com/shareArticle?mini=true&url={{ get_permalink() }}&title={{ get_the_title() }}" target="_blank" style="color: #636363;"><i class="fab fa-linkedin"></i></a>
```

Add Google fonts:
In setup.php right under namespace App > use ...... :
```
function google_fonts_url()
{
    return 'https://fonts.googleapis.com/css?family=' . urlencode('Montserrat:400,600|Roboto:300,400&display=swap');
}
```
in setup.php right above the wp_enqueue_style('sage/main.css', line under add_action('wp_enqueue_scripts', function:
```
wp_enqueue_style('google/fonts', \App\google_fonts_url(), false, null);
```

