# SCSS Grid System

Bu SCSS tabanlı grid sistemi, özelleştirilebilir breakpoint değerleri ile birlikte kullanılmak üzere tasarlanmıştır.

## Kullanım

Öncelikle, projenizin ana SCSS dosyasında aşağıdaki gibi breakpoint değerlerini tanımlayın:

```scss
// media breakpoints
$breakpoints: (
  'xs': 29.6875em,
  'sm': 40em,
  'md': 48em,
  'lg': 64em,
  'xl': 80em,
  'xxl': 96em,
  'xxxl': 100em,
) !default;

```scss
@include breakpointMaxWidth(sm) {
  // Ekran genişliği sm breakpoint'inin üzerine çıktığında uygulanacak stil
  // Örnek: @media screen and (max-width: 40em) { ... }
  .element {
    // Stil tanımlamaları
  }
}

```scss
@include breakpointMinWidth(md) {
  // Ekran genişliği md breakpoint'inin altına indiğinde uygulanacak stil
  // Örnek: @media screen and (min-width: 48em) { ... }
  .element {
    // Stil tanımlamaları
  }
}