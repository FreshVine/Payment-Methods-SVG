# Payment Methods SVG
A Simple set of Payment Method icons with an SVG stylish approach. This approach allows us the scaling benefits of a web-font (vectors!), but with the ability to correctly color match to the brand specifications. It also retains the ease of use by having a css library which you can drop into your project. Yet it will be flexible enough for you to easily adapt, select, and tailor to your site.  

The `lib/paymentMethods.min.css` file is only 30kb (12.7KB with gzip) and includes the 6 payment methods marks accepted by stripe. The card version of the same library - `lib/paymentMethods.cards.min.css` - is 120kb (40.9KB with gzip) due to increased SVG complexity.
  
The goal here is to also present each brand according to their brand guidelines. While this does take away some of the creativity from the presentation it should allow for simple implementation to meet the terms of accepting their methods.  
  
[View Demo - https://freshvine.github.io/Payment-Methods-SVG/](https://freshvine.github.io/Payment-Methods-SVG/) 

**Icons Available**  
Below are the links to the SVG files. This is to show the artwork used since you cannot add a stylesheet to a ReadMe. [View the demo](https://freshvine.github.io/Payment-Methods-SVG/) to see the css library in action.  
<img src="https://raw.githubusercontent.com/FreshVine/Payment-Methods-SVG/master/icons/marks/amex.svg?sanitize=true" height="50"> <img src="https://raw.githubusercontent.com/FreshVine/Payment-Methods-SVG/master/icons/marks/diners-club.svg?sanitize=true" height="50"> <img src="https://raw.githubusercontent.com/FreshVine/Payment-Methods-SVG/master/icons/marks/discover.svg?sanitize=true" height="50"> <img src="https://raw.githubusercontent.com/FreshVine/Payment-Methods-SVG/master/icons/marks/jcb.svg?sanitize=true" height="50"> <img src="https://raw.githubusercontent.com/FreshVine/Payment-Methods-SVG/master/icons/marks/mastercard.svg?sanitize=true" height="50"> <img src="https://raw.githubusercontent.com/FreshVine/Payment-Methods-SVG/master/icons/marks/visa.svg?sanitize=true" height="50">  
  
<img src="https://raw.githubusercontent.com/FreshVine/Payment-Methods-SVG/master/icons/cards/amex.svg?sanitize=true" height="50"> <img src="https://raw.githubusercontent.com/FreshVine/Payment-Methods-SVG/master/icons/cards/diners-club.svg?sanitize=true" height="50"> <img src="https://raw.githubusercontent.com/FreshVine/Payment-Methods-SVG/master/icons/cards/discover.svg?sanitize=true" height="50"> <img src="https://raw.githubusercontent.com/FreshVine/Payment-Methods-SVG/master/icons/cards/jcb.svg?sanitize=true" height="50"> <img src="https://raw.githubusercontent.com/FreshVine/Payment-Methods-SVG/master/icons/cards/mastercard.svg?sanitize=true" height="50"> <img src="https://raw.githubusercontent.com/FreshVine/Payment-Methods-SVG/master/icons/cards/visa.svg?sanitize=true" height="50">  
  
**Approach Icons**  
<img src="https://raw.githubusercontent.com/FreshVine/Payment-Methods-SVG/master/icons/cards/apple-pay.svg?sanitize=true" height="50"> <img src="https://raw.githubusercontent.com/FreshVine/Payment-Methods-SVG/master/icons/cards/pay-with-google.svg?sanitize=true" height="50">  

## Payment Methods Included  

[American Express](https://www.americanexpress.com), [Diner Club](https://www.dinersclub.com/), [Discover](https://www.discover.com/), [JBC](http://www.global.jcb/), [MasterCard](http://www.mastercard.com/), and [Visa](https://www.visa.com/).

### Tokenized Payment Approaches

A tokenized payment approach allows the user to pay you, but without giving you their card information. Instead a single use token is generated that allows you to charge them. The main approaches here are Apple Pay, and Pay with Google. For these approaches only Cards are provided as neither Apple or Google have a mark for you to use. These card icons are not forced to the same dimensions as the normal cards.

[Apple Pay](https://www.apple.com/apple-pay/), [Pay with Google](https://www.google.com/payments/solutions/#apps-mobile-web)

## Using the Library

There are two steps to using the Payment Methods SVG library. First is you must include a css file. Second you need to add a properly classed element to your DOM. The icon will be the height of the font where it is placed. To adjust the size simply adjust the font size of the element (or its parent element), or you can adjust the height of the element.

**Step 1:** Add the Stylesheet to your page header.  

	<link rel="stylesheet" href="lib/paymentMethods.min.css">

**Step 2:** Add an Element with the correct classes. I'm partial to `<i>`.

	<i class="paymentMethod amex"></i>
	<i class="paymentMethod amex paymentMethod-card"></i>


### Class Guide

*	***paymentMethod***: This defines the base for the icon. Ensure that it behaves as you would expect inline.  
*	***paymentMethod-card***: Will use the card icon if it is included, or will default back to the mark icon.  
*	***disabled***: A simple disabled state which desaturates the icon, and drops the opacity.  

Each payment method has its own class [*ex:* amex, visa]. Look at the included sample if you cannot figure out which class goes with which icon.


## The Icons  

For the sake of consistency every icon is going to have the same dimensions of 85.60 mm × 53.98 mm (the same as a credit card). We are not using an image sprite, but instead will embed a base encoded version of the svg file into the computed css.  

This minimizes the number of requests (helpful for mobile) and is just my preference. While this will result in a larger css file, svg images are normally quite smaller than their raster friends. This also allows for more true drag and drop performance.  

### Mark Icons  
These are the standard icons used by default. It is expected that these logos will appear on a white, or light colors background (for when there are options darker marks are selected). These icons are not uniform in width, but have the same height. The rough goal is to give each logo around 3250 mm² of area (where the height is 50mm and width would be 65mm).  
  
With icons which are wider they will not span the full vertical height in order to achieve the same rough visual weight as other more square shaped marks. These wider marks should be vertically centered in the space.  

### Card Icons  
These are designed to look like credit cards to further highlight the main branding colors of each payment method. They are uniform in size and share the same card shape. The brand mark on the card is sized to carry a similar visual weight, and to feel similar to the rest of the cards. The background of the card is informed by the branding guidelines for each method.  
  
Often the brand will supply a color, graphic, or full art to use for this approach. These tend to look like the graphics you would see on stickers next to a register or in a shop window.  

### Notes on Artwork

#### Visa
There are a lot of visa logos floating around. One that we saw frequently was the blue word mark with the gold point on the upper left of the V. However the brand guidelines we could access directly from Visa were using the one we have placed.

### Notes on Conversions to SVG

#### Discover
So the vector discover logo makes use of several multiplication layers. This is a problem since there is no direct way to convert a these layers to SVG which does not have native layer blending modes. Instead of messing with svg filters which might have gotten us close we simple disabled these layers. This gets us very close, but without the shadow on the upper left corner of the mark, or the more burnt umber color on the upper left third. This decision was reached when the SVG on the Discover site was using a rasterized image that was then clipped for the mark.


## Prebuilt Libraries

We will include 4 pre-built libraries for ease of use: stripe-marks (`lib/paymentMethods.min.css`), stripe-cards  (`lib/paymentMethods.cards.min.css`), all-marks (`lib/paymentMethods.all.min.css`), and all-cards (`lib/paymentMethods.all.cards.min.css`). The stripe libraries will only include Visa, MasterCard, American Express, Diners Club, JCB and Discover. These are the methods accepted by Stripe.

## Making your own Library  

Every icon will have it's own `*.scss` file which is included or excluded in the building process. This level of flexibility allows you to easily include/exclude the payment methods you need or not. 

**Example:** `/project-payment-methods.scss`

	// Bring in the Payment Method base style builder
	@import 'path-to-project/style/builder';

	//
	// Import the specific payment methods we are using
	@import 'path-to-project/icons/marks/amex';
	@import 'path-to-project/icons/marks/diners-club';
	@import 'path-to-project/icons/marks/discover';
	@import 'path-to-project/icons/marks/jcb';
	@import 'path-to-project/icons/marks/mastercard';
	@import 'path-to-project/icons/marks/visa';

	@import 'path-to-project/icons/cards/mastercard';
	@import 'path-to-project/icons/cards/visa';


## Building the Precompiled Libraries

In the `style/` directory are 4 `*.scss` files which we use to build out our precompiled libraries. The sass commands below will compile them when executed from the root of this project.  

	sass style/all.cards.scss lib/paymentMethods.all.cards.min.css --style compressed --sourcemap=none
	sass style/all.cards.scss lib/paymentMethods.all.cards.css --style expanded
	sass style/all.scss lib/paymentMethods.all.min.css --style compressed --sourcemap=none
	sass style/all.scss lib/paymentMethods.all.css --style expanded

	sass style/stripe.cards.scss lib/paymentMethods.cards.min.css --style compressed --sourcemap=none
	sass style/stripe.cards.scss lib/paymentMethods.cards.css --style expanded  
	sass style/stripe.scss lib/paymentMethods.min.css --style compressed --sourcemap=none
	sass style/stripe.scss lib/paymentMethods.css --style expanded  

	sass style/all.approaches.scss lib/paymentApproaches.all.cards.min.css --style compressed --sourcemap=none
	sass style/all.approaches.scss lib/paymentApproaches.all.cards.css --style expanded  
	sass style/stripe.approaches.scss lib/paymentApproaches.cards.min.css --style compressed --sourcemap=none
	sass style/stripe.approaches.scss lib/paymentApproaches.cards.css --style expanded  

## Requesting the addition of a Payment Method  

Our desire is to see the supported methods grow. To make a request open an issue and include a link to a published art/resources from the brand in question. We will not use links to third party sites to craft icons in this project.  

If you notice that one of the icons we are using is out of date please open an issue pointing us to updated art/resources.

## Resources
The artwork, design, and rights to these marks remains with the individual brands. They make this work available so that we can correctly represent their brands where their cards are accepted. These are the locations where we access their vector artwork. If there is more current documentation or brand guidelines please let us know - we will update accordingly.

*	[American Express](https://merchant-supplies.americanexpress.com/?locale=en_US#/catalog/producttype/digitalsigns)  
*	[Apple Pay](https://developer.apple.com/apple-pay/web-human-interface-guidelines/)  
*	[Diners Club](https://www.discovernetwork.com/en-us/business-resources/free-signage-logos)  
*	[Discover](https://www.discovernetwork.com/en-us/business-resources/free-signage-logos)  
*	[Google - Pay with Google](https://developers.google.com/payments/brand-guidelines#pay-with-google-brand-assets)
*	[JBC](http://www.jcb.co.jp/bdmanual/en/index.html)  
*	[MasterCard](https://brand.mastercard.com/brandcenter/mastercard-brand-mark/downloads.html)  
*	[Visa](https://www.visaeurope.com/receiving-payments/pos_branding) with [branding guide](https://www.visa.ca/dam/VCOM/download/merchants/New_VBM_Acq_Merchant_62714_v5.pdf)  
