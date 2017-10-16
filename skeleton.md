What happens to the layout when you resize the screen to less than 550 px? How do you think that works?

On getskeleton.com when the window is reduced to less than 550 px, the layout changes. The most notable change is that images that were side by side, have now been re-orientated to be one on top of the other.

I think this works by having an @media query for a specific screen size (in this case 550 px) and a new rule set in that screen size. My guess is the code looks something like this


@media (min width 550px){
box-width: 90%;

}

below is the correct code copied from the source:
@media (min-width: 550px) {
  .section {
    padding: 12rem 0 11rem;
  }
  .hero {
    padding-bottom: 12rem;
    text-align: left;
    height: 165px;
  }
  .phone {
    position: absolute;
    top: -7rem;
    right: 3rem;
    max-height: 362px;
    z-index: 3;
  }
  .phone + .phone {
    top: -6rem;
    display: block;
    max-width: 73.8%;
    right: 0;
    z-index: 2;
    max-height: 338px;
  }
  .hero-heading {
    font-size: 2.4rem;
  }
}



/* Larger than phone */
@media (min-width: 550px) {
  .header {
    margin-top: 18rem; }
  .value-props {
    margin-top: 9rem;
    margin-bottom: 7rem; }
  .value-img {
    margin-bottom: 1rem; }
  .example-grid .column,
  .example-grid .columns {
    margin-bottom: 1.5rem; }
  .docs-section {
    padding: 6rem 0; }
  .example-send-yourself-copy {
    float: right;
    margin-top: 12px; }
  .example-screenshot-wrapper {
    position: absolute;
    width: 48%;
    height: 100%;
    left: 0;
    max-height: none; }
