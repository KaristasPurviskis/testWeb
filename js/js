document.addEventListener('DOMContentLoaded', () => {
  // Timeline animation
  const timelineItems = document.querySelectorAll('.timeline-item');
  
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        entry.target.classList.add('visible');
      }
    });
  }, {
    threshold: 0.2,
    rootMargin: '0px 0px -100px 0px'
  });

  timelineItems.forEach((item, index) => {
    // Instantly show the first two timeline items
    if (index < 2) {
      item.classList.add('visible');
    } else {
      observer.observe(item);
    }
  });
});


document.querySelectorAll('.read-more-btn').forEach(button => {
  button.addEventListener('click', () => {
    const fullText = button.previousElementSibling;
    const shortText = button.parentElement.querySelector('.short-text');

    if (fullText.style.display === 'none') {
      fullText.style.display = 'block';
      shortText.style.display = 'none';
      button.textContent = 'Rādīt mazāk';
    } else {
      fullText.style.display = 'none';
      shortText.style.display = 'block';
      button.textContent = 'Lasīt vairāk';
    }
  });
});