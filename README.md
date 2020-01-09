# sage_customisations
Roots/Sage Customisations

Lightweight facebook and liknedin share button on any post:

```
<a href="https://www.facebook.com/sharer.php?u={{ get_permalink() }}" target="_blank" style="color: #636363;"><i class="fab fa-facebook"></i></a>

<a href="https://www.linkedin.com/shareArticle?mini=true&url={{ get_permalink() }}&title={{ get_the_title() }}" target="_blank" style="color: #636363;"><i class="fab fa-linkedin"></i></a>
```
