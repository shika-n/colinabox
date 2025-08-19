<script>
import { browser } from "$app/environment";
import Quagga from "@ericblade/quagga2";

if (browser) {
	const msg = document.querySelector("#message");
	Quagga.init({
		inputStream: {
			name: "live",
			type: "LiveStream",
			target: "#stream",
		},
		locator: {
			halfSample: true,
			patchSize: "medium",
		},
		decoder: {
			readers: [ "ean_reader" ],
			debug: {
				drawBoundingBox: true,
				drawScanline: true,
				showFrequency: true,
				showPattern: true,
			}
		}
	}, (err) => {
		if (err) {
			if (msg) {
				msg.textContent = err;
			}
			return;
		}
		if (msg) {
			msg.textContent = "Quagga ready!";
		}
		Quagga.start();
	});
	Quagga.onProcessed((data) => {
		console.log("proc: ", data);
	})
	Quagga.onDetected((data) => {
		console.log("detect: ", data);
	})
}
</script>

<div>
	<button onclick={() => Quagga.start()}>Scan</button>
	<button onclick={() => Quagga.pause()}>Stop</button>
	<span id="message"></span>
	<div id="stream">Stream</div>
</div>
