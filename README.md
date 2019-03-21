<!DOCTYPE html>
    <head>
        <title></title>
    </head>
    <link rel="stylesheet" href="bower_components/bootstrap/dist/css/bootstrap.min.css">
    <script src="bower_components/jquery/dist/jquery.min.js"></script>
    <body>
        <div class="container">
                <div class="col-sm-6">
                    <label for="">Product: </label>
                    <input type="text" id="Product" placeholder="Product Name"><br>
                    <label for="">Price: </label>
                    <input type="text" id="Price" placeholder="Enter Price"><br>
                    <label for="">Quantity: </label>
                    <input type="text" id="Quantity" placeholder="Enter Quantity"><br>
                    <button id="submit" class="btn btn-primary">Submit</button>
                    <hr>
                    <table class="table table-bordered">
                        <thead>
                            <tr>
                                <th>Product</th>
                                <th>Price</th>
                                <th>Quantity</th>
                                <th>Total</th>
                            </tr>
                        </thead>
                        <tbody id="database">

                        </tbody>
                    </table>
                </div>
            </div>
        <script>
            var btnadd = document.getElementById('submit');
            btnadd.addEventListener('click', function(){
                var content=document.getElementById('database');

                var Product=document.getElementById('Product').value;
                var Price=Number(document.getElementById('Price').value);
                var Quantity=Number(document.getElementById('Quantity').value);
                var sum = Price * Quantity;
                var newentry="<tr>" + "<td>" + Product + "</td>" + "<td>" + Price + "</td>" + "<td>" + Quantity + "<td>" + sum +"</td>" + "</tr>";
                content.insertAdjacentHTML('afterbegin', newentry);
            });
        </script>
    </body>
</html>
