<!-- @format -->
<template>
	<div
		id="appex"
		:class="[{ preloading: !isPreloading }, { loaded: isLoaded }]"
	>
		<!-- <svg
			style="width:0;height:0;position:absolute;"
			aria-hidden="true"
			focusable="false"
		>
			<linearGradient
				id="dorado"
				x1="0%"
				y1="0%"
				x2="100%"
				y2="0%"
				gradientTransform="rotate(135)"
			>
				<stop offset="0%" style="stop-color:#FCDD8C;stop-opacity:1" />
				<stop offset="50%" style="stop-color:#ffffff;stop-opacity:1" />
				<stop offset="100%" style="stop-color:#CB851F;stop-opacity:1" />
			</linearGradient>
		</svg>
		<nav class="navegacion">
			<h1 class="logo">
				<a href="/">
					<svgicon class="icon" data-size="_65" name="logo_m" />
				</a>
			</h1>
			<ul :class="[{ is_open: mNavOpen }, 'menu', 'nav']">
				<li :class="{ active: activo == 'home' }">
					<a
						:data-gradient="c.title.a"
						@click.prevent="moveTo('#')"
						href="#"
					>
						{{ c.title.a }}
					</a>
				</li>
				<li :class="{ active: activo == 'about-us' }">
					<a
						:data-gradient="c.title.b"
						@click.prevent="moveTo('#about-us')"
						href="#about-us"
					>
						{{ c.title.b }}
					</a>
				</li>
				<li :class="{ active: activo == 'benefits' }">
					<a
						:data-gradient="c.title.c"
						@click.prevent="moveTo('#benefits')"
						href="#benefits"
					>
						{{ c.title.c }}
					</a>
				</li>
				<li :class="{ active: activo == 'requirements' }">
					<a
						:data-gradient="c.title.d.short"
						@click.prevent="moveTo('#requirements')"
						href="#requirements"
					>
						{{ c.title.d.short }}
					</a>
				</li>
				<li :class="{ active: activo == 'contact' }">
					<a
						:data-gradient="c.title.e"
						@click.prevent="moveTo('#contact')"
						href="#contact"
					>
						{{ c.title.e }}
					</a>
				</li>
			</ul>
			<ul class="nav hamburguer">
				<li v-if="mNavOpen">
					<a href="#" @click.prevent="mNavOpen = false">
						<i
							data-gradient
							class="fas fa-times icon"
							data-size="_25"
						></i>
					</a>
				</li>
				<li v-else>
					<a href="#" @click.prevent="mNavOpen = true">
						<i
							data-gradient
							class="fas fa-bars icon"
							data-size="_25"
						></i>
					</a>
				</li>
			</ul>
		</nav> -->
		<section id="matriz" class="views">
			<div id="home" class="tab is_tope" @mouseenter="setActive('home')">
				<article class="wrapper">
					<div class="holder" data-layout="title">
						<div class="title">
							<span>Lago UV</span>
							<span>Victor Saa</span>
						</div>
					</div>
				</article>
				<div class="aside forward">
					<div class="holder">
						<span>Escena</span>
						<h3>01</h3>
						<a
							href="#escena-02"
							class="side_action"
							@click.prevent="moveTo('#escena-01')"
						>
							<i
								class="fas fa-arrow-right icon"
								data-size="_25"
							></i>
						</a>
					</div>
				</div>
			</div>
			<div
				id="escena-01"
				class="tab"
				@mouseenter="setActive('escena-01')"
			>
				<!-- <div class="aside back">
					<div class="holder">
						<span>Escena</span>
						<h3>02</h3>
						<a
							href="#"
							class="side_action"
							@click.prevent="moveTo('#')"
						>
							<i
								data-gradient
								class="fas fa-arrow-left icon"
								data-size="_25"
							></i>
						</a>
					</div>
				</div> -->
				<article class="wrapper"></article>
				<div class="aside forward">
					<div class="holder">
						<span>Escena</span>
						<h3>02</h3>
						<a
							href="#benefits"
							class="side_action"
							@click.prevent="moveTo('#escena-02')"
						>
							<i
								class="fas fa-arrow-right icon"
								data-size="_25"
							></i>
						</a>
					</div>
				</div>
			</div>
			<div
				id="escena-02"
				class="tab"
				@mouseenter="setActive('escena-02')"
			>
				<!-- <div class="aside back">
					<div class="holder">
						<span>Escena</span>
						<h3>04</h3>
						<a
							href="#about-us"
							class="side_action"
							@click.prevent="moveTo('#about-us')"
						>
							<i
								data-gradient
								class="fas fa-arrow-left icon"
								data-size="_25"
							></i>
						</a>
					</div>
				</div> -->
				<article class="wrapper"></article>
				<div class="aside forward">
					<div class="holder">
						<span>Escena</span>
						<h3>03</h3>
						<a
							href="#requirements"
							class="side_action"
							@click.prevent="moveTo('#escena-03')"
						>
							<i
								class="fas fa-arrow-right icon"
								data-size="_25"
							></i>
						</a>
					</div>
				</div>
			</div>
			<div
				id="escena-03"
				class="tab"
				@mouseenter="setActive('escena-03')"
			>
				<!-- <div class="aside back">
					<div class="holder">
						<span :data-gradient="c.title.c">{{ c.title.c }}</span>
						<h3 data-gradient="02">02</h3>
						<a
							href="#benefits"
							class="side_action"
							@click.prevent="moveTo('#benefits')"
						>
							<i
								data-gradient
								class="fas fa-arrow-left icon"
								data-size="_25"
							></i>
						</a>
					</div>
				</div> -->
				<article class="wrapper"></article>
				<div class="aside forward">
					<div class="holder">
						<span>Escena</span>
						<h3>04</h3>
						<a
							href="#contact"
							class="side_action"
							@click.prevent="moveTo('#escena-04')"
						>
							<i
								class="fas fa-arrow-right icon"
								data-size="_25"
							></i>
						</a>
					</div>
				</div>
			</div>
			<div
				id="escena-04"
				class="tab"
				@mouseenter="setActive('escena-04')"
			>
				<div class="aside back">
					<div class="holder">
						<span>
							Volver al inicio
						</span>
						<h3>00</h3>
						<a
							href="#requirements"
							class="side_action"
							@click.prevent="moveTo('#home')"
						>
							<i
								class="fas fa-arrow-left icon"
								data-size="_25"
							></i>
						</a>
					</div>
				</div>
				<article class="wrapper"></article>
			</div>
		</section>
		<!-- <footer class="inferior">
			<ul class="social">
				<li>
					<a
						href="https://www.instagram.com/goldenberry_studio/"
						target="_blank"
					>
						<i
							data-gradient
							class="fab fa-instagram icon"
							data-size="_25"
						></i>
					</a>
				</li>
				<li>
					<a
						href="https://www.facebook.com/goldenberrystudio/"
						target="_blank"
					>
						<i
							data-gradient
							class="fab fa-facebook-square icon"
							data-size="_25"
						></i>
					</a>
				</li>
			</ul>
		</footer> -->
	</div>
</template>

<script>
	// import Hello from './components/HelloWorld.vue'
	export default {
		name: "App",
		components: {
			// Hello
		},
		data() {
			return {
				// variable: 'valor',
				isPreloading: true,
				isLoaded: false,
				activo: "home",
				ventana: null,
				mNavOpen: false,
			};
		},
		computed: {
			// computado(){
			// 	//contenido
			// },
			is_touch() {
				return "ontouchstart" in window ? true : false;
			},
		},
		created() {
			//free land
			let _this = this;
			_this.ventana = window.innerWidth;
			_this.activo = window.location.hash;

			// setTimeout(function(){
			// 	// console.log(_this.isPreloading);
			// 	_this.isPreloading = false;
			// }, 1000);
			setTimeout(function() {
				// console.log('t1');
				_this.isPreloading = false;
				// setTimeout(function(){
				// 	console.log('t2');
				_this.isLoaded = true;
				// }, 300);
			}, 1200);
			// console.log(_this.is_touch);
			// var myScroll = new IScroll('#matriz', {
			// 	scrollX: true,
			// 	scrollY: false,
			// 	mouseWheel: true,
			// 	scrollbars: true
			// });
			// const softScroll = (e) => {
			// 	// let _this = this;
			// 	const delta = Math.sign(e.deltaY);
			// }
			// const d_SoftScroll = _this.debounced(200, softScroll);
			// window.addEventListener("wheel", d_SoftScroll); //mejorara o buscar mejor alternativa
			// window.addEventListener('wheel', e => {
			// 	const delta = Math.sign(e.deltaY);
			// 	console.info(delta);
			// 	console.log(e);
			// 	// return
			// 	// $('.views').scrollLeft -= (delta * 50);
			//  // event.preventDefault();
			// });
			// $(function() {
			// 	$('html, body .views').mousewheel(function(event, delta) {
			// 		this.scrollLeft -= (delta * 50);
			// 		event.preventDefault();
			// 	});
			// });

			// window.addEventListener('scroll', () => {
			// 	// console.log('hi');
			// 	// _this.fixedNav = $(window).scrollTop() >= 80;
			// }, 1000);
			// const wSize = (e) => {
			// 	// let _this = this;
			// 	// const delta = Math.sign(e.deltaY);
			// 	_this.ventana = window.innerWidth;
			// }
			// const d_wSize = _this.debounced(200, wSize);
			// window.addEventListener('resize', d_wSize);
			window.addEventListener(
				"resize",
				_this.debounced(200, e => {
					// console.log('resize');
					_this.ventana = window.innerWidth;
				})
			);
			if (!_this.is_touch) {
				window.addEventListener(
					"wheel",
					_this.debounced(7, _this.scrollHorizontally)
				);
			}
			window.addEventListener("hashchange", e => {
				// console.log('url change');
				// console.log(window.location);
				_this.moveTo(window.location.hash, true);
				// builder(window.location.pathname);
			});
			// if (document.getElementById('matriz').addEventListener) {
			// 	// IE9, Chrome, Safari, Opera
			// 	document.getElementById('matriz').addEventListener("mousewheel", _this.scrollHorizontally, false);
			// 	// Firefox
			// 	document.getElementById('matriz').addEventListener("DOMMouseScroll", _this.scrollHorizontally, false);
			// } else {
			// 	// IE 6/7/8
			// 	document.getElementById('matriz').attachEvent("onmousewheel", _this.scrollHorizontally);
			// }
		},
		beforeDestroy() {
			window.removeEventListener("resize");
			window.removeEventListener("wheel");
			window.removeEventListener("hashchange");
		},
		methods: {
			// metodo: function(section) {
			// 	let _this = this;
			// 	//tu funcion
			// 	return
			// },
			debounced: function(delay, fn) {
				let timerId;
				return function(...args) {
					if (timerId) {
						clearTimeout(timerId);
					}
					timerId = setTimeout(() => {
						fn(...args);
						timerId = null;
					}, delay);
				};
			},
			scrollHorizontally: function(e) {
				let _this = this;
				e = window.event || e;
				if (_this.ventana > 720) {
					//ajustar segun responsive
					var delta = Math.max(
						-1,
						Math.min(1, e.wheelDelta || -e.detail)
					);
					document.getElementById("matriz").scrollLeft -= delta * 70; // Multiplied by 40
					// e.preventDefault();
				}
			},
			moveTo: function(section, i) {
				// console.log("f u");
				let _this = this;
				// console.log('scrolling babe to: '+section);
				_this.mNavOpen = false;
				if ((section === "#") | (section === "")) {
					_this.activo = "home";
					if (_this.ventana > 720) {
						// console.log('tLeft');
						$(".views").animate({ scrollLeft: 0 }, 300, "swing");
					} else {
						// console.log('ttop');
						$("html, body").animate({ scrollTop: 0 }, 300, "swing");
					}
				} else {
					var nPosition =
						_this.ventana > 720
							? $(".views " + section).position().left
							: $(".views " + section).position().top;
					// var nPosition = $('.views '+section).position().left - $('.views').position().left;
					// var nPosition = $('.views '+section).offset().top - $('.views '+section).offsetParent().offset().top;
					// var nts = $(section).position();
					// console.log($(section).position().left);
					// console.log('child offset: '+nPosition+' y parent scrollLeft: '+$('.views').scrollLeft());
					// console.log('np: '+nPosition+';offset: '+$('.views').scrollLeft());
					if (nPosition != 0) {
						_this.activo = section.replace(/#/gi, "");
						if (_this.ventana > 720) {
							// console.log($('.views').scrollLeft() + nPosition);
							$(".views").animate(
								{
									scrollLeft:
										$(".views").scrollLeft() + nPosition,
								},
								300
							);
						} else {
							// console.log('tmov');
							$("html, body").animate(
								{
									scrollTop:
										$(".views").scrollTop() + nPosition,
								},
								300
							);
						}
					}
				}
				if (!i) {
					history.pushState("", document.title, "/" + section);
				}
				return false;
			},
			setActive: function(activeTab) {
				let _this = this;
				// console.log(activeTab);
				if (_this.activo !== activeTab) {
					_this.activo = activeTab;
					history.pushState("", document.title, "/#" + activeTab);
				}
				return;
			},
		},
	};
</script>
