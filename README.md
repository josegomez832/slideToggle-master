# slideToggle

##HTML Setup
```
<div class="title" id="question1">Question Here</div>
<div class="question1 content">Content</div>
```

##JQuery

```javascript
$('.content').hide();
$('.title').click(function(e){
  var id = this.id;
  var opened = $(this).hasClass('clicked');
  e.preventDefault();
  $('.clicked').removeClass('clicked');
  $('.content').slideUp();
               
  if(!opened){
    //$(this).removeClass('clicked');
    $(this).addClass('clicked');
    $('.content.'+ id).slideDown();
    //console.log('fired');
	}  
})
``` 