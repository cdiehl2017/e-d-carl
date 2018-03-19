# e-d-carl
CodeLouisville project that I created to showcase my son's artwork. This is just a simple site that will eventually be completely rewritten to become his resume/portfolio with future animation work.

I took inpsiration from an older theme I had when I first started to play with coding and I added a gallery for his work and a form to allow emails to be sent to him requesting information.

Some of my CSS classes are gallery, media, media all originals, media all fanart, content. These set the gallery in flex style display and allows them to be divided by genre and to open from thumb to full

	.gallery {
		padding: 3.5em;
		position: relative;
		overflow: hidden;
		min-height: 37em;
	}

	.gallery .content {
			display: -ms-flexbox;
			display: -moz-flex;
			display: -webkit-flex;
			display: -ms-flex;
			display: flex;
			-moz-flex-wrap: wrap;
			-webkit-flex-wrap: wrap;
			-ms-flex-wrap: wrap;
			flex-wrap: wrap;
			-moz-justify-content: -moz-flex-start;
			-webkit-justify-content: -webkit-flex-start;
			-ms-justify-content: -ms-flex-start;
			justify-content: flex-start;
		}

My gallery javascript allows the the images to separated and opend by genre and to open in a popup lightbox with captions for the artwork.

		$gallery.each( function() {

						var $this = $(this),
							$tabs = $this.find('.tabs a'),
							$media = $this.find('.media');

						$tabs.on('click', function(e) {

							var $this = $(this),
								tag = $this.data('tag');
                
                					$content.poptrox({
						usePopupCaption: true
					});
