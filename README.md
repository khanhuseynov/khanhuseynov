 <p class="typed-text"></p>


    <style>
        p{
            font-family: 'Courier New', Courier, monospace;
            font-size: 30px;
            color: brown;
        }
    </style>



    <script>
        const typedText = document.querySelector('.typed-text');

const textArray = ['HI', 'I AM KHAN', 'I AM JUNIOR FRONTEND DEVELOPER'];
let textIndex = 0;
let charIndex = 0;

function type() {
  if (charIndex < textArray[textIndex].length) {
    typedText.textContent += textArray[textIndex].charAt(charIndex);
    charIndex++;
    setTimeout(type, 100);
  } else {
    setTimeout(erase, 1000);
  }
}

function erase() {
  if (charIndex > 0) {
    typedText.textContent = textArray[textIndex].substring(0, charIndex - 1);
    charIndex--;
    setTimeout(erase, 100);
  } else {
    textIndex++;
    if (textIndex >= textArray.length) textIndex = 0;
    setTimeout(type, 1000);
  }
}

type();

    </script>

