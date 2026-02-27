const message = `I don't even know if you'll read this but I hope you do, Bunga.\nI just want you to know, if we're here! There's me, Ifah, Keyla.\n\nThe four of us have been trying to stay together. The three of us also care about you and you're not alone ♡. No one can predict the future, but the universe never gives us enough space to be the "best" version of us.\n\nI'll just say that if we meet at different points in life, it doesn't limit our friendship.\n\nAnyway, I hope you're okay, even though you and we are in a sad and down state. But, I hope the four of us will always be one and not forget each other. be happy Bunga Clarizha Hartono.`;

function showLetter() {
  document.getElementById("introText").style.opacity = 0;
  document.querySelector(".btn").style.display = "none";

  setTimeout(() => {
    const letterBox = document.getElementById("letterBox");
    const typedText = document.getElementById("typedText");
    letterBox.style.display = "block";
    let i = 0;

    function typeWriter() {
      if (i < message.length) {
        typedText.innerHTML += message.charAt(i);
        i++;
        setTimeout(typeWriter, 30);
      }
    }

    typeWriter();
  }, 600);
}
