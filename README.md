# bootstrap-reference

Smooth Scrolling

//Add smooth scrolling
$('#main-nav a').on('click',function(e) {
  //Check hash value
  if(this.hash!=='')
  {
    e.preventDefault();
    //Store hash
    const hash=this.hash;
    //Animate smooth scroll
    $('html, body').animate({
      scrollTop:$(hash).offset().top
    },900,function(){
      window.location.hash=hash;
    })
  }
})
