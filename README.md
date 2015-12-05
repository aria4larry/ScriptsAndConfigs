# ScriptsAndConfigs
use full scripts and configs


<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>smart query</title>
</head>
<body>
<h1>smart query</h1>
    <input type="text" class="form-control" id="smartqueryresult" placeholder="Enter value">
    <button type="button" class="btn btn-primary" id="btn_smartquery">smart query</button>
    <script src="jquery.min.js"></script>
    <script type="text/javascript">
        $(document).ready(
               function() {
                    $("#btn_smartquery").click(
                            function() {
                                window.opener.postMessage("what does the fox say","*");
                            });
               });
     </script>
</body>
</html>


<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>pdas cherry pick</title>
</head>
<body>
    <h1>cherry pick</h1>
    <input type="text" class="form-control" id="smartqueryresult" placeholder="Enter value">
    <button type="button" class="btn btn-primary" id="search" data-loading-text="Saving...">smart search</button>
    <script src="jquery.min.js"></script>
    <script type="text/javascript">
     $(document).ready(
     function() {
         $("#search").click( 
             function() {
                 winAddTestPlan = window
                         .open('http://mcdat03:8080/mocksq/smartquery.html', 'pdaCreateTestPlan',
                    'location=no, menubar=no, scrollbars=no, status=no, toolbar=no');
                 window.addEventListener('message', function(event) {
                     $('#smartqueryresult').val(event.data)
                     winAddTestPlan.close();
                 });
             });
     });
    </script>
</body>
</html>
