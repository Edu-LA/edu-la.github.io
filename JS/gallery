const images = document.querySelectorAll('.gallery-image');
const captions = document.querySelectorAll('.caption-text');
const prevBtn = document.querySelector('.gallery-nav.prev');
const nextBtn = document.querySelector('.gallery-nav.next');
const currentCounter = document.querySelector('.current-image');
const totalCounter = document.querySelector('.total-images');

let currentIndex = 0;
const totalImages = images.length;

totalCounter.textContent = totalImages;


function showImage(index) {
    
    images.forEach(img => img.classList.remove('active'));
    captions.forEach(caption => caption.style.display = 'none');

    images[index].classList.add('active');
    captions[index].style.display = 'block';
    
    currentCounter.textContent = index + 1;
}


nextBtn.addEventListener('click', () => {
    currentIndex++;
    if (currentIndex >= totalImages) {
        currentIndex = 0; 
    }
    showImage(currentIndex);
});


prevBtn.addEventListener('click', () => {
    currentIndex--;
    if (currentIndex < 0) {
        currentIndex = totalImages - 1; 
    }
    showImage(currentIndex);
});


document.addEventListener('keydown', (e) => {
    if (e.key === 'ArrowRight') {
        nextBtn.click();
    } else if (e.key === 'ArrowLeft') {
        prevBtn.click();
    }
});