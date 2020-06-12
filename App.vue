<script>
	export default {
		onLaunch: function() {
			console.log('App Launch')
		},
		onShow: function() {
			console.log('App Show')
		},
		onHide: function() {
			console.log('App Hide')
		}
	}
</script>

<style>
	/*每个页面公共css */
	    @font-face {font-family: "iconfont";
	      src: url('~@/static/fonts/iconfont.eot?t=1576335469449'); /* IE9 */
	      src: url('~@/static/fonts/iconfont.eot?t=1576335469449#iefix') format('embedded-opentype'), /* IE6-IE8 */
	      url('data:application/x-font-woff2;charset=utf-8;base64,d09GMgABAAAAAAVMAAsAAAAAChwAAAT/AAEAAAAAAAAAAAAAAAAAAAAAAAAAAAAAHEIGVgCDKAqHQIYhATYCJAMUCwwABCAFhG0HUBurCFGUTk6f7EeBu6eIlFFajBY208XLlGHx/6/hiYfvx76d+2xFJLlUn75pp4tCoyQ8NgiJUJjuJfzNpSrpXIDoeDbs3GjyH7Lfv+zTy1mok+GyEhYAW8AKaPvz/6eeG1QvDUo6SQW8bE4KYTDSMRj1R/5x7/TP88Dmo7Jc/misYXOelwWYYEBjbGxrAQ7KEvQW8SwuJBO4nkCvRQ21q/PbB5hXQLdAvDU6gHmbRQnhhG598xlb1lEvsu70PvEBfFU/H/+hF1IkNYO+149nMRz+6v7/fwrv4JAqI6T5uXCbRMYWUIhnX8+tKT22ZUrvJ3PaCdCNryR+Sb2RfRPT+c9kbdF0s788siIRDWj6GXkWL/ySEsVkfsmyftoYKiIZsiQfJ+Y2ll7MgdgDiE/AMF+CumLWsCSpdFXpjsNkefoatW8WSY8xapRhreWm1a9vWvVEM6edaQdPapImTzTLLG4BwEBG/HJsK4bVEKkStJbxbUYy3othvO2ofJA7jBARcUZ4illDuEL29TB2C/3AGWj4WUfGYbG25LTICaEk1jWBR8KWC0bqQJ+EjJYmOnvisiHzqtifvZ08X7NYzBaJWAJBglDIRIi3Fd/C3cbZjqEKvkh9Qmx2SKCgMAhD15VHVkCQMCWOP72YnLB0euHUpROzJ/PEYiR6wxK8ShC+ZsryVibGlbIzorOjqRKnhwyOKTIlMRoPSLgMlYvInDIKdwsQ8K2YbO2PReRsyxzZvrK0dWxUYUrIE2sPj8+sHNw6tUVhj0AgslvelUfhDnNG4k0YwgedbyX/ovPRL8SnqwOt/atMII/RGGMacyXGJOaq+MtGYDFMOL1Hk8OSJdfqARNMZkPmnDVh5DP0bjDpx6XAB6RO0JkqM4F0fNSNZMKXB20QqI//n+swdzCvnv1/JszOzMEszPsskD8RZtrarNB14gGhubjWlduokVnWD9e9PyCQd1jtvPjStKTGs6VZFT/xjhhW0hpkG6PoC0wW8iGUrPK9prFY4AM+9GF8APhKfIvr5tct+IoAxU/eE3ILa4yrDxTgUfkrG0lPTtshU4pGtXT9UJqywWkDhzyi/5ka15D+WlPn1Gd+QYF7s0j3dXTuS0oStZLum6on86NOwIbPcydIP3+STiDFaYk1Z6WFLPt7b7M6EhMA+Gr+qtDilfia4mPFr0p8JZUS973QHulzYJxsPjJ6xdeW7Wd75WHHrZsGDXaUb1hacCuQVmrOkt1DjdgTxSeY3EcWDqCzRLxB9PmH2DNplYhzhCDbNLfzY7dKy1jb/dqNFfBTXbWg8vhWsH1JP9IN0VQmIcif4isHay1vtVDzNIiyxeirbpZ0JKEXg3QAAqN+8jFMLN9E6DZhQtJlAbJuS2ght6DqcwRNt1Potelicp8xbEqUHmz4IBCGfUIy6DtkwyZoIb+hmvQLzXAQoddNbM3ZZyWKFk+YAqEYwxGayJZKsMuiVnxH2ucBW+Uq94m4MkHstjrO5AWVxHkMqPq6J6JQsS3wnGxGeW7RsU0pklYi4rbbbeV3plZkC1h0iZGAIDEUGkFGxCopubpYdL3/DtG8XIBDSn4knxBWMbWjrpZODPRCU8YqWZfGlT6tRwjFOynMKqBz6iI5xizk/FulSES0JCkizrY2q6Tialrl64ppLD0VysKcNVLkKFGjae8S40w5K14OB+WS9lKjkR/YgsrZsRnZzAAA') format('woff2'),
	      url('~@/static/fonts/iconfont.woff?t=1576335469449') format('woff'),
	      url('~@/static/fonts/iconfont.ttf?t=1576335469449') format('truetype'), /* chrome, firefox, opera, Safari, Android, iOS 4.2+ */
	      url('~@/static/fonts/iconfont.svg?t=1576335469449#iconfont') format('svg'); /* iOS 4.1- */
	    }
	
	    .iconfont {
	      font-family: "iconfont" !important;
	      font-size: 16px;
	      font-style: normal;
	      -webkit-font-smoothing: antialiased;
	      -moz-osx-font-smoothing: grayscale;
	    }
	
	    .icon-shipin:before {
	      content: "\f0024";
	    }
	
	    .icon-tupian:before {
	      content: "\e650";
	    }
	
	    .icon-guanyuwomen:before {
	      content: "\e608";
	    }
	
	    .icon-ziyuan:before {
	      content: "\e60d";
	    }
		.gomeImgLoad{
			width: 750rpx;
			height: auto;
		}
</style>
