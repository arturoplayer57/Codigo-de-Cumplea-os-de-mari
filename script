document.addEventListener('DOMContentLoaded', () => {
  const cards = document.querySelectorAll('.envelope-card');
  const modal = document.getElementById('photoModal');
  const closeModal = document.getElementById('closeModal');
  const modalImg = document.getElementById('modalImg');
  const modalTitle = document.getElementById('modalTitle');
  const modalDesc = document.getElementById('modalDesc');

  // Lanzar un poco de confeti al cargar la página
  setTimeout(() => {
    launchConfetti();
  }, 500);

  // Al hacer clic en una carta/sobre
  cards.forEach(card => {
    card.addEventListener('click', () => {
      const imgSrc = card.getAttribute('data-img');
      const title = card.getAttribute('data-title');
      const desc = card.getAttribute('data-desc');

      modalImg.src = imgSrc;
      modalTitle.textContent = title;
      modalDesc.textContent = desc;

      modal.classList.add('active');
      launchConfetti();
    });
  });

  // Cerrar el modal al hacer clic en el botón (X)
  closeModal.addEventListener('click', () => {
    modal.classList.remove('active');
  });

  // Cerrar el modal al hacer clic fuera del contenido
  modal.addEventListener('click', (e) => {
    if (e.target === modal) {
      modal.classList.remove('active');
    }
  });

  // Función para disparar confeti
  function launchConfetti() {
    if (typeof confetti === 'function') {
      confetti({
        particleCount: 80,
        spread: 70,
        origin: { y: 0.6 },
        colors: ['#f8a5c2', '#f78fb3', '#ffffff', '#ffd1dc', '#f368e0']
      });
    }
  }
});
