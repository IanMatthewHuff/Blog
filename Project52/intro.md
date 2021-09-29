## Project 52 - Computer generated playing card deck

This is a project I've been looking to put together for a little while. Basically a way to practice different computer generated techniques and technology while still working toward a cohesive final product. I'm going to walk along with the entire process on the blog and share the various cards as they are developed as well as the final product.

### Concept / Motivation

I've always been interested in computer generated art, but there are so many different technologies and techniques out there. I was looking for a way to play around with lots of different techniques, but all with something that's part of the same goal or project, as opposed to just aimless noodling. I enjoy boardgames as well as custom decks of cards, after a bit of thinking combining the two seemed like a perfect fit. I could have a set output, a fixed image size, plus a template for the suit / rank, and then use whatever I wanted to generate that image.

### Output Target

From a few sources online I picked [MakePlayingCards.com](https://www.makeplayingcards.com/design/custom-blank-card.html) as my target printer. The reputation was there, and they had lots of printing options and templates, as well as reasonable prices for small batches. From their [templates](https://www.makeplayingcards.com/pops/faq-photo.html) I could select a target resolution to use for this. The template lists 300 dpi as the minimum to use, since my art should be able to scale to any range (as I'm generating it) I bumped this up to 900 dpi. I'm not a print / graphical design expert, but this just felt like more detail flexibility and a smooth scaling ratio. One website online mentioned 800 dpi for tarot sized cards from this site, so 900 for poker size should be more than enough.

The given stats on the site is 822 x 1122 (36 pixel bleed on all edges) for a 300dpi poker size card. So to bump that up we're looking at a 2466 x 3366 for the initial card target that I'm going to look at.

### Individual Cards

Each card can be a totally isolated project, as long as it get our output image to the right size. This frees me up to play around with different techniques and technologies for creating each piece of art. For a hobby project when you have limited time it feels important to me to be able to play around like this, and still have individually achievable chunks of work that I can accomplish. I'm interesting in playing around with Processing (Python + Javascript), Cairo, and maybe dipping back into my DX / OpenGL past some.

### Card Template

At the same time as starting to generate cards, I also want to look at a meta program for creating the full deck. Basically I want this template to have fonts / icons for the suits and ranks. Then I want this program to process over all the images to overlay the suit into in the corners. Considerations here might include something like borders to set apart the suit info as well as either finding open source icons and fonts or designing some of my own. But this step can come along at the same time as the cards are getting created.
