@import "minimal-mistakes";

html {
  font-size: 11px; // change to whatever

  @include breakpoint($medium) {
    font-size: 11px; // change to whatever
  }

  @include breakpoint($large) {
    font-size: 13px; // change to whatever
  }

  @include breakpoint($x-large) {
    font-size: 15px; // change to whatever
  }
}