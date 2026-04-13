# 📋 Project Overview — CSS Flag Design (Flag of Laos)

## 🎯 Goal
This project teaches **CSS positioning techniques and selector specificity** by recreating a real national flag using nothing but nested `<div>` elements styled with CSS. No images, no JavaScript, no Bootstrap.

## 📄 HTML Structure (Fixed — Do Not Modify)
```html
<body>
  <div class="flag">         ← Outer container (red background)
    <p>The Flag</p>          ← White text on red
    <div>                    ← Blue middle band
      <div>                  ← White circle
        <p>of Laos</p>       ← Black text in circle
      </div>
    </div>
  </div>
</body>
```

## 🧠 CSS Solution Explained

### Layer 1: The Flag Container
```css
.flag {
  height: 600px;
  width: 900px;
  position: relative;        /* allows positioning children absolutely */
  background-color: #ce1126; /* Laos red */
}
```

### Layer 2: The Blue Middle Band
```css
.flag > div {
  /* targets ONLY the direct div child of .flag */
  background-color: #002868;  /* Laos blue */
  position: absolute;
  top: 150px;     /* 1/4 of 600px = 150px */
  height: 300px;  /* half the flag height */
  width: 900px;   /* full width */
}
```

### Layer 3: The White Circle
```css
.flag > div div {
  background-color: #ffffff;
  height: 200px;
  width: 200px;
  border-radius: 50%;         /* makes a perfect circle */
  position: absolute;
  left: 350px;    /* (900 - 200) / 2 = 350px to center horizontally */
  top: 50px;      /* (300 - 200) / 2 = 50px to center vertically */
}
```

### Text Styling
```css
p {
  color: #ffffff;
  text-align: center;
  font-size: 5rem;
}

.flag > div > div p {
  color: black;   /* text inside the white circle is black */
}
```

## 🔑 Key Technique: CSS Combinators
| Selector | Meaning |
|---|---|
| `.flag > div` | Direct child div of `.flag` |
| `.flag > div div` | Any div inside `.flag`'s child div |
| `.flag > div > div p` | `<p>` inside the white circle |

This teaches **specificity** without needing class or ID attributes.

## 📊 Difficulty Level
| Aspect | Rating |
|---|---|
| HTML | ⭐ (fixed, don't touch) |
| CSS | ⭐⭐⭐ (position, border-radius, combinators) |
| Math | ⭐⭐ (calculating center positions) |
| Overall | ⭐⭐ Beginner-Intermediate |

## 💡 Next Steps
- Try recreating the flag of Japan (just a circle on white)
- Try the flag of France (3 vertical stripes — great Flexbox practice!)
- Try the flag of Bangladesh (circle off-center)
- Add CSS hover animations
