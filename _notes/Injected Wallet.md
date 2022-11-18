## Inject Provider
Todas las browser wallet inyectan un objeto en el HTML.

## HTML
```HTML
<body>
	<button id="botonConectar" onclick="conectar()">
		CONECTAR
	</button>
	<script>
		async function conectar() {
			if (typeof window.ethereum !== "undefined") {
				await ethereum.request(
					{method:"eth_requestAccounts"}
				)
			}
		}
	</script>
</body>
```