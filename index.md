<!DOCTYPE html>
<html>
<head>
	<meta name="viewport" content="width=device-width, initial-scale=1">
	<link rel="stylesheet" href="css.css">
	<link rel="stylesheet" href="https://cielyozora.github.io/rpwradio-drama/css.css">
	<title>Dane Lattimoreroror</title>
	<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.12.4/jquery.js"></script>
</head>
<body>
<form action="https://script.google.com/macros/s/AKfycbwd1HhdPhMY2Kl0DIt6DQrmOTy018_ERanlVgiFlpF4K7FARDJ-GHDg/exec" id="form" method="post">
  
  <h1><strong>Final</strong> Recordings</h1>
  <div id="data"></div>
  <div class="form-group">
    <label for="title">Line Number <span>Enter the number of your line</span></label>
    <input type="text" name="linenumber" id="title" class="form-controll"/>
  </div>
  <div class="form-group">
    <label for="caption">Character <span>Enter your character name</span></label>
    <input type="text" name="character" id="caption" class="form-controll"/>
  </div>
  
  <div class="form-group file-area">
        <label for="images">Recordings <span>Upload the final take of your recording</span></label>
    <input type="file" name="file" id="uploadfile" required="required" multiple="multiple"/>
    <div class="file-dummy">
      <div class="success">Great, your files are selected. Keep on.</div>
      <div class="default">Please select some files</div>
    </div>
  </div>
  
  <div class="form-group">
    <button type="submit" id="submit" onclick="submitform();">Upload Recordings now</button>
  </div>
  
</form>
<link href='https://fonts.googleapis.com/css?family=Lato:100,200,300,400,500,600,700' rel='stylesheet' type='text/css'>

<a href="https://facebook.com/rpwradio.official" class="back-to-article" target="_blank">Facebook</a>


      <script>
    $('#uploadfile').on("change", function() {
        var file = this.files[0];
        var fr = new FileReader();
        fr.fileName = file.name;
        fr.onload = function(e) {
            e.target.result
            html = '<input type="hidden" name="data" value="' + e.target.result.replace(/^.*,/, '') + '" >';
            html += '<input type="hidden" name="mimetype" value="' + e.target.result.match(/^.*(?=;)/)[0] + '" >';
            html += '<input type="hidden" name="filename" value="' + e.target.fileName + '" >';
            $("#data").empty().append(html);
        }
        fr.readAsDataURL(file);
    });
    </script>
<script type="text/javascript">
function submitform() {

document.getElementById('#form').submit();
}
</script>
</body>
</html>
