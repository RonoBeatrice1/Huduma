jQuery(window).on('load', function() {

	initIsoTop();
	// IsoTop init
	function initIsoTop() {
		"use strict";

		var isotopeHolder = jQuery('.isoContentHolder'),
			win = jQuery(window);
		jQuery('.isoFiltersList a').on( "click", function(e){
			e.preventDefault();
			
			jQuery('.isoFiltersList li').removeClass('active');
			jQuery(this).parent('li').addClass('active');
			jQuery('.widgetFiltersNav').removeClass('openActive');
			var selector = jQuery(this).attr('data-filter');
			isotopeHolder.isotope({ filter: selector });
		});
		jQuery('.isoContentHolder').isotope({
			itemSelector: '.isoCol',
			transitionDuration: '0.6s',
			masonry: {
				columnWidth: '.isoCol'
			}
		});
	}

	if(jQuery(window).width() < 992){
		jQuery('.widgetFiltersNav > h3').on('click', function(){
			jQuery(this).parents('.widgetFiltersNav').toggleClass('openActive');
		});
	}

	jQuery( "#loader" ).delay( 600 ).fadeOut( 300 );

});

jQuery(document).ready(function(){

	initHasHover();
	// add classes on hover/touch
	function initHasHover() {
		jQuery('.hasOver').touchHover({});
	}

	initStickyScrollBlock();
	// initialize fixed blocks on scroll
	function initStickyScrollBlock() {
		jQuery('.sSticky').stickyScrollBlock({
			setBoxHeight: true,
			activeClass: 'fixed-position',
			positionType: 'fixed'
		});
	}

	jQuery('.dropdown-submenu > a').on("click", function(e){
	   jQuery(this).next('.dropdown-menu').parent('li').toggleClass('show');
	   jQuery(this).next('.dropdown-menu').toggleClass('show');
	   e.stopPropagation();
	   e.preventDefault();
	});

	jQuery(".vssDropdownHolder").hover(
		function () {
			jQuery('.vssOpener', this).addClass('hover');
		},

		function () {
			jQuery('.vssOpener', this).removeClass('hover');
		}
	);

	initCounter();
  	// Counter init
  	function initCounter() {
		// jQuery('.counter').counterUp({
		// 	delay: 10,
		// 	time: 2000
		// });

	   jQuery('.dataCount').counterUp({
	   	delay: 10,
	   	time: 1260
	   });

	   jQuery('.dataCountBar').counterUp({
	      delay: 1,
	      time: 50
	   });
  	}

	initProgressBar();
	// Progress Bar init
	function initProgressBar() {
		if( jQuery(".progress-bar").length != '' ){
			var waypoint = new Waypoint({
				element: document.getElementById('progress-bar'),
				handler: function(direction) {
					console.log('Scrolled to startpoint!');
					jQuery('.progress-bar .progressBar').each(function() {
							var widthBar = jQuery(this).find('.over').attr('data-percent');
							jQuery(this).find('.over').animate({
								'width': widthBar
							});
					});
				},
				offset: '80%'
			});
		}
	}

	initAnchors();
	// initialize smooth anchor links
	function initAnchors() {
		new SmoothScroll({
			anchorLinks: 'a.smooth[href^="#"]:not([href="#"])',
			extraOffset: 0,
			wheelBehavior: 'none',
			animMode: 'duration',
			animDuration: 1000
		});
	}

	initFancybox();
	// lightbox init
	function initFancybox() {
		jQuery('a.lightbox, [data-fancybox]').fancybox({
			parentEl: 'body',
			margin: [50, 0],
			gutter: 0,
			slideShow: false
		});
	}

	initSlickCarousel();
	// initSlickCarousel init
	function initSlickCarousel() {
		jQuery('.ibSlider').slick({
			slidesToShow: 1,
			slidesToScroll: 1,
			dots: false,
			arrows: true,
			prevArrow: '<a href="#" class="slickPrev ssArrowVi rounded-circle d-flex align-items-center justify-content-center fas fa-chevron-left position-absolute"><span class="sr-only">prev</span></a>',
			nextArrow: '<a href="#" class="slickNext ssArrowVi rounded-circle d-flex align-items-center justify-content-center fas fa-chevron-right position-absolute"><span class="sr-only">next</span></a>',
			autoplay: true,
			fade: true,
			speed: 1300,
			adaptiveHeight: true,
			autoplaySpeed: 10000,
			responsive: [{
				breakpoint: 768,
				settings: {
					arrows: false,
					dots: true,
					dotsClass: 'dotsList d-flex align-items-center justify-content-center list-unstyled mb-0'
				}
			}]
		});

		jQuery('.echSlider').slick({
			slidesToShow: 1,
			slidesToScroll: 1,
			dots: true,
			arrows: false,
			centerMode: true,
			centerPadding: '0px',
			dotsClass: 'dotsList dotsListii d-flex align-items-center justify-content-center list-unstyled mb-0 mt-8 mt-lg-12'
		});

		jQuery('.echSlidervii').slick({
			slidesToShow: 2,
			slidesToScroll: 1,
			dots: false,
			arrows: false,
			responsive: [
				{
					breakpoint: 576,
					settings: {
						slidesToShow: 1,
						slidesToScroll: 1,
					}
				}
			]
		});

		jQuery('.testimonialSlider').slick({
			slidesToShow: 3,
			slidesToScroll: 1,
			arrows: false,
			dots: true,
			dotsClass: 'dotsList dotsListii d-flex align-items-center justify-content-center list-unstyled mb-0 mt-4 mt-lg-8',
			responsive: [
				{
					breakpoint: 992,
					settings: {
						slidesToShow: 2,
						slidesToScroll: 1,
					}
				},
				{
					breakpoint: 768,
					settings: {
						slidesToScroll: 1,
						slidesToShow: 1,
					}
				}
			]
		});

		jQuery('.arddColumnSlider').slick({
			slidesToShow: 3,
			slidesToScroll: 3,
			arrows: true,
			prevArrow: '<a href="#" class="slickPrev ssArrowVii rounded-circle d-flex align-items-center justify-content-center fas fa-chevron-left position-absolute"><span class="sr-only">prev</span></a>',
			nextArrow: '<a href="#" class="slickNext ssArrowVii rounded-circle d-flex align-items-center justify-content-center fas fa-chevron-right position-absolute"><span class="sr-only">next</span></a>',
			dots: true,
			dotsClass: 'dotsList dotsListii d-flex align-items-center justify-content-center list-unstyled mb-0 mt-4 mt-lg-8',
			responsive: [
				{
					breakpoint: 1230,
					settings: {
						slidesToShow: 2,
						slidesToScroll: 2,
					}
				},
				{
					breakpoint: 992,
					settings: {
						arrows: false,
						slidesToShow: 2,
						slidesToScroll: 2,
					}
				},
				{
					breakpoint: 768,
					settings: {
						slidesToScroll: 1,
						slidesToShow: 1,
					}
				}
			]
		});

		jQuery('.lgsImagesSlider').slick({
			slidesToShow: 5,
			slidesToScroll: 1,
			dots: false,
			arrows: false,
			responsive: [{
				breakpoint: 992,
				settings: {
					slidesToShow: 3,
					slidesToScroll: 1,
				}
			}]
		});

		jQuery('.dcsInnSlider').slick({
			slidesToShow: 1,
			slidesToScroll: 1,
			dots: false,
			arrows: true,
			prevArrow: '<a href="#" class="slickPrev ssArrowVii rounded-circle d-flex align-items-center justify-content-center fas fa-chevron-left position-absolute"><span class="sr-only">prev</span></a>',
			nextArrow: '<a href="#" class="slickNext ssArrowVii rounded-circle d-flex align-items-center justify-content-center fas fa-chevron-right position-absolute"><span class="sr-only">next</span></a>',
			autoplay: false,
			fade: true
		});

		jQuery('.scgSpeakersSlider').slick({
			slidesToShow: 3,
			slidesToScroll: 3,
			dots: true,
			dotsClass: 'dotsList dotsListii d-flex align-items-center justify-content-center list-unstyled mb-0 mt-n12',
			arrows: false,
			responsive: [{
				breakpoint: 992,
				settings: {
					slidesToShow: 2,
					slidesToScroll: 2,
				}
			}]
		});

		jQuery('.nrcImageSlider').slick({
			slidesToShow: 1,
			slidesToScroll: 1,
			dots: false,
			arrows: true,
			prevArrow: '<a href="#" class="slickPrev ssArrowVii rounded-circle d-flex align-items-center justify-content-center fas fa-chevron-left position-absolute"><span class="sr-only">prev</span></a>',
			nextArrow: '<a href="#" class="slickNext ssArrowVii rounded-circle d-flex align-items-center justify-content-center fas fa-chevron-right position-absolute"><span class="sr-only">next</span></a>',
			autoplay: false,
			fade: true
		});

		jQuery('.quotesSlider').slick({
			slidesToShow: 1,
			slidesToScroll: 1,
			dots: true,
			arrows: false,
			autoplay: false,
			dotsClass: 'dotsList dotsListii d-flex align-items-center justify-content-center list-unstyled mb-0 mt-8 mt-lg-12',
		});
	}

	jQuery('.parallaxWindow').parallax();

	// addToCart Quantity Input
	jQuery('.quantity-button#plus').on('click', function () {
		if (jQuery(this).prev().val() < 3) {
			jQuery(this).prev().val(+jQuery(this).prev().val() + 1);
		}
	});

	jQuery('.quantity-button#minus').on('click', function () {
		if (jQuery(this).next().val() > 1) {
		if (jQuery(this).next().val() > 1)
			jQuery(this).next().val(+jQuery(this).next().val() - 1);
		}
	});

	jQuery('.mainNavigation .nav-link[href^="#"]').each(function(){
		jQuery(this).on('click', function(){
			event.preventDefault();
			var hash = this.hash;

			jQuery('html, body').animate({
				scrollTop: jQuery(hash).offset().top
			}, 800, 'swing');
		})
	})

});

/*quantity input number custom pluggin*/
jQuery('<div class="quantity-nav"><div class="quantity-button quantity-plus d-flex align-items-center justify-content-center"><i class="fas fa-caret-up"><span class="sr-only">icon</span></i></div><div class="quantity-button quantity-minus d-flex align-items-center justify-content-center"><i class="fas fa-caret-down"><span class="sr-only">icon</span></i></div></div>').insertAfter('.quantity input');
jQuery('.quantity').each(function() {
	var spinner = jQuery(this),
		input = spinner.find('input[type="number"]'),
		btnUp = spinner.find('.quantity-plus'),
		btnDown = spinner.find('.quantity-minus'),
		min = input.attr('min'),
		max = input.attr('max');

	btnUp.on('click', function() {
		var oldValue = parseFloat(input.val());
		if (oldValue >= max) {
			var newVal = oldValue;
		} else {
			var newVal = oldValue + 1;
		}
		spinner.find("input").val(newVal);
		spinner.find("input").trigger("change");
	});

	btnDown.on('click', function() {
		var oldValue = parseFloat(input.val());
		if (oldValue <= min) {
			var newVal = oldValue;
		} else {
			var newVal = oldValue - 1;
		}
		spinner.find("input").val(newVal);
		spinner.find("input").trigger("change");
	});
});

$(function() {
	$( "#slider-range" ).slider({
		range: true,
		min: 0,
		max: 60,
		values: [ 10, 35 ],
		slide: function( event, ui ) {
			$( "#amount" ).html( "Price : $" + ui.values[ 0 ] + " — $" + ui.values[ 1 ] );
	$( "#amount1" ).val(ui.values[ 0 ]);
	$( "#amount2" ).val(ui.values[ 1 ]);
		}
	});
	$( "#amount" ).html( "Price : $" + $( "#slider-range" ).slider( "values", 0 ) +
	" — $" + $( "#slider-range" ).slider( "values", 1 ) );

	$( "#amount1" ).val($( "#slider-range" ).slider( "values", 10 ));
	$( "#amount2" ).val($( "#slider-range" ).slider( "values", 35 ));
});


jQuery(document).ready(function(){
	initCountdown100();
  // Counter init
  function initCountdown100() {

  }
});

jQuery(document).ready(function(){
	initCountdown100();
  // Counter init
   function initCountdown100() {
 		jQuery('.cd100').countdown100({
		/*Set Endtime here*/
		/*Endtime must be > current time*/
		endtimeYear: 0,
		endtimeMonth: 0,
		endtimeDate: 18,
		endtimeHours: 12,
		endtimeMinutes: 6,
		endtimeSeconds: 30,
		timeZone: "" 
		// ex:  timeZone: "America/New_York"
		//go to " http://momentjs.com/timezone/ " to get timezone
	});
  }
});
