<!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>MARKET TRACK: MONITORING COST CHANGES ACROSS GRICULTURE PRODUCT CHANNELS</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-KK94CHFLLe+nY2dmCWGMq91rCGa5gtU4mk92HdvYe+M/SXH301p5ILy+dN9+nJOZ" crossorigin="anonymous">
  </head>
  <style>
		h1 {
			color: rgb(0, 0, 0);
			text-align: center;
		}

		.warning {
			color: red;
			font-weight: bold;
			text-align: center;
		}
		.card{
		margin-left:410px;
		margin-top: 20px;
		display: flex;
		flex-direction: row;
		align-items: center;
		color: rgb(241, 239, 240);
		}
		.container{
		background:#fffbfe;
		font-weight: bold;
		padding-bottom:10px;
		border-radius: 15px;
		}
	</style>




  <body style="background:#BCBBB8">
  <!--=======================navbar=====================================================-->
<nav class="navbar navbar-expand-lg navbar-dark bg-dark">
  <div class="container-fluid">
    <a class="navbar-brand" href="/">MARKET TRACK: MONITORING COST CHANGES ACROSS GRICULTURE PRODUCT CHANNELS</a>
  </div>
</nav>

<!--==========================================================================================-->
  <div class="container my-3 mt-3">
      <h1 class="text-success">MARKET TRACK: MONITORING COST CHANGES ACROSS GRICULTURE PRODUCT CHANNELS<span class="text-success">🌱</span></h1>

<!--      adding form-->
      <form action="/predict" method="POST">
          <div class="row">
              <div class="col-md-4">
					<label for="Nitrogen">Nitrogen</label>
					<input type="number" id="Nitrogen" name="Nitrogen" placeholder="Enter Nitrogen" class="form-control" required step="0">
				</div>
               <div class="col-md-4">
					<label for="Phosporus">Phosphorus</label>
					<input type="number" id="Phosporus" name="Phosporus" placeholder="Enter Phosphorus" class="form-control" required step="00">
				</div>
				<div class="col-md-4">
					<label for="Potassium">Potassium</label>
					<input type="number" id="Potassium" name="Potassium" placeholder="Enter Potassium" class="form-control" required step="0">
				</div>
          </div>

          <div class="row mt-4">
				<div class="col-md-4">
					<label for="Temperature">Temperature</label>
					<input type="number" step="0.01" id="Temperature" name="Temperature" placeholder="Enter Temperature in °C" class="form-control" required step="0">
				</div>
				<div class="col-md-4">
					<label for="Humidity">Humidity</label>
					<input type="number" step="0.01" id="Humidity" name="Humidity" placeholder="Enter Humidity in %" class="form-control" required step="0">
				</div>
				<div class="col-md-4">
					<label for="pH">pH</label>
					<input type="number" step="0.01" id="pH" name="pH" placeholder="Enter pH value" class="form-control" required step="0">
				</div>
			</div>

          <div class="row mt-4">
				<div class="col-md-4">
					<label for="Rainfall">Rainfall</label>
					<input type="number" step="0.01" id="Rainfall" name="Rainfall" placeholder="Enter Rainfall in mm" class="form-control" required>
				</div>
			</div>



           <div class="row mt-4">

           <div class="col-md-12 text-center">
				<button type="submit" class="btn btn-primary btn-lg">Get Recommendation</button>
			</div>
			</div>
      </form>

       {% if result %}
		<div class="card bg-dark" style="width: 18rem;">
		  <img src="{{url_for('static', filename='crop.png')}}" style="width: 70px; height: 70px;" class="card-img-top" alt="...">
		  <div class="card-body">
			<h5 class="card-title">Recommend Crop for Cultivation is:</h5>
			<p class="card-text">{{ result }} </p>
		  </div>
		</div>
	   {% endif %}
  </div>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha3/dist/js/bootstrap.bundle.min.js" integrity="sha384-ENjdO4Dr2bkBIFxQpeoTz1HIcje39Wm4jDKdf19U8gI4ddQ3GYNS7NTKfAdVQSZe" crossorigin="anonymous"></script>
  </body>
</html>
