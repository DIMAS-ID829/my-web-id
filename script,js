// Tahun otomatis footer
document.getElementById('year').textContent = new Date().getFullYear();

// mobile menu toggle
(function(){
  var hambtn = document.getElementById('hambtn');
  var nav = document.getElementById('mobilenav');
  hambtn.addEventListener('click', function(){
    if(nav.style.display === 'block'){
      nav.style.display = 'none';
    } else {
      nav.style.display = 'block';
    }
  });

  // hide on resize > show proper nav
  window.addEventListener('resize', function(){
    if(window.innerWidth > 820){
      nav.style.display = 'none';
    }
  });
})();

// add to cart simple UX
function addCart(e){
  try {
    var btn = e.currentTarget || e.target;
    var name = btn.getAttribute('data-name') || 'Product';
    // lightweight toast-like feedback
    var toast = document.createElement('div');
    toast.textContent = name + ' added to cart ✓';
    toast.style.position = 'fixed';
    toast.style.right = '20px';
    toast.style.bottom = '20px';
    toast.style.background = 'rgba(0,0,0,0.85)';
    toast.style.color = '#fff';
    toast.style.padding = '10px 14px';
    toast.style.borderRadius = '10px';
    toast.style.zIndex = 9999;
    toast.style.fontSize = '13px';
    toast.style.transition = 'opacity 0.3s';
    document.body.appendChild(toast);
    setTimeout(function(){
      toast.style.opacity = '0';
      setTimeout(()=>toast.remove(),300)
    }, 1600);
  } catch(err){
    console.error(err);
    alert('Added to cart');
  }
}

// Scroll ke section dengan smooth
function scrollToSection(id){
  var el = document.querySelector(id);
  if(el) el.scrollIntoView({behavior:'smooth', block:'start'});
}
// Ads Slider Logic
(function() {
  const slides = document.querySelectorAll('.ad-slide');
  const prevBtn = document.querySelector('.ad-nav.prev');
  const nextBtn = document.querySelector('.ad-nav.next');
  let current = 0;
  let timer;
