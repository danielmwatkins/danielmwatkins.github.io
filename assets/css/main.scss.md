@import "minimal-mistakes";

html {
  font-size: 14px; // change to whatever

  @include breakpoint($medium) {
    font-size: 12px; // change to whatever
  }

  @include breakpoint($large) {
    font-size: 14px; // change to whatever
  }

  @include breakpoint($x-large) {
    font-size: 20px; // change to whatever
  }
}