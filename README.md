# Babykit
Dit zou eerst een CSS only opdracht worden maar ik heb later wat JavaScript toegevoegd.

```JavaScript
function flesSchudden() {

    let random = Math.floor(Math.random() * (80 - 10)) + 10;
    console.log(random, -random);

    base = 'translatey(0) rotate(0)';
    rotateLeft = `translateY(-30%) rotate(-${random}deg)`;
    rotateRight = `translateY(-30%) rotate(${random}deg)`;

    fles.animate([
        { transform: base, offset: 0 },
        { transform: rotateRight, offset: .3 },
        { transform: rotateLeft, offset: .5 },
        { transform: rotateRight, offset: .7 },
        { transform: rotateLeft, offset: .9 },
        { transform: base, offset: 1 }

    ], {
        duration: 1200,
        iterations: 1,
        easing: 'ease-in-out'
    });

    document.querySelector('.melk').animate([
        { transform: 'translateY(0) scale(0.3, 1)', borderRadius: '50% / 67% 67% 33% 33%', opacity: 1 },
        { transform: 'translateY(-35vh) scale(2, 0.4)', borderRadius: '50% / 33% 33% 67% 67%', opacity: .2 }
    ], {
        duration: 350,
        delay: 700,
        iterations: 2,
        easing: 'ease-in-out'
    });
};
```
