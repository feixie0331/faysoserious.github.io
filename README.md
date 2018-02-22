<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="utf-8">
		<title>D3: Setting paragraphs' style conditionally, based on data</title>
		<script type="text/javascript" src="../d3.js"></script>
	</head>
	<body>
		<script type="text/javascript">
		
			var dataset = [ 5, 10, 15, 20, 25 ];
			
			d3.select("body").selectAll("p")
				.data(dataset)
				.enter()
				.append("p")
				.text(function(d) {
					return "I can count up to " + d;
				})
				.style("color", function(d) {
					if (d > 15) {	//Threshold of 15
						return "red";
					} else {
						return "black";
					}
				});
			
		</script>
	</body>
</html>
