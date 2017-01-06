# Owl Carousel-2 With Bootstrap Tab

It's Very Easy To Use Responsive Bootstrap Tab With Owl Carousel2. Just Follow The Instructions .....

```javascript

initialize_owl($('.product-carousel-wrapper'));

$('a[href="#mobile-tablet"]').on('shown.bs.tab', function () {
   initialize_owl($('.product-carousel-wrapper'));
}).on('hide.bs.tab', function () {
   destroy_owl($('.product-carousel-wrapper'));
});

$('a[href="#computer"]').on('shown.bs.tab', function () {
   initialize_owl($('.product-carousel-wrapper2'));
}).on('hide.bs.tab', function () {
   destroy_owl($('.product-carousel-wrapper2'));
});

function initialize_owl(el) {

   el.owlCarousel({
     loop       : true,
     margin     : 30,
     dots       : false,
     mouseDrag  : false,
     responsive : {
       0 : {
         items : 1
       },
       480 : {
         items : 1
       },
       678 : {
         items :4
       },
       960 : {
         items : 5
       }
     }
   });
}

function destroy_owl(el) {
   el.trigger("destroy.owl.carousel");
   el.find('.owl-stage-outer').children(':eq(0)').unwrap();
}
```
