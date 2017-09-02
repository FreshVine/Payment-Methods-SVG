# Payment Methods SVG
A Simple set of Payment Method icons with an SVG stylish approach. This approach allows us the scaling benifits of a webfont (vectors!), but with the ability to correctly color match to the brand specifications. It also retains the ease of use by having a css library which you can drop into your project.



## The Icons

For the sake of consisency every icon is going to have the same dimensions of 85.60 mm × 53.98 mm (the same as a credit card). We are not using an image sprite, but instead will embed a base encoded version of the svg file into the computed css.  

This minimizes the number of requests (helpful for mobile) and is just my preference. While this will result in a larger css file, svg images are normally quite smaller than their raster friends. This also allows for more true drag and drop performance.  

### Mark Icons
These are the standard icons used by default. They will only be the individual marks for each payment method. 

## Making your own Library

Every icon will have it's own `*.scss` file which is included or excluded in the buildling process. This level of flexibilty allows you to easily include/exclude the payment methods you need or not. We will include 3 pre-bunlded scripts for ease of use: minimal-mark, minimal-card, and full (every icon madem, in both formats). The minimal scripts will only include Visa, MasterCard, American Express, Diners Club, JCB and Discover. These are the methods accepted by Stripe.


## Resources
The artwork, design, and rights to these marks remains with the individual brands. They make this work available so that we can correctly represent their brands where their cards are accepted. These are the locations where we access their vector artwork.

*	American Express  
*	Diners Club  
*	Discover  
*	JBC  
*	[Mastercard](https://brand.mastercard.com/brandcenter/mastercard-brand-mark/downloads.html)  
*	[Visa](https://www.visaeurope.com/receiving-payments/pos_branding) with [branding guide](https://www.visa.ca/dam/VCOM/download/merchants/New_VBM_Acq_Merchant_62714_v5.pdf)  