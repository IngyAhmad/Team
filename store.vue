
<template>
<html>
<div class="container">

<head>
<link href="//maxcdn.bootstrapcdn.com/bootstrap/3.3.0/css/bootstrap.min.css" rel="stylesheet" id="bootstrap-css">
<link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.4.0/css/font-awesome.min.css" rel='stylesheet' type='text/css'>
</head>

    <div class="row">

        <div class="col-md-10 col-md-offset-1">

            <div class="panel panel-default panel-table">
              <div class="panel-heading">
                <div class="row">
                  <div class="col col-xs-6">
                    <h3 class="panel-title">Products</h3>
                  </div>
                  <div class="col col-xs-6 text-right">
                    <button type="button" class="btn btn-sm btn-primary btn-create" @click="myFunction()" >Create New</button>
                    <button type="button" class="btn btn-sm btn-primary btn-create" @click="myFunction1()">Update Product</button>
                    <button type="button" class="btn btn-sm btn-primary btn-create">View Products</button>
                    <form id="product-form" role="form" style="display: none;">
                      <h2>NEW PRODUCT</h2>
                        <div class="form-group">
                          <input type="text" name="Name" id="name" tabindex="1" class="form-control" placeholder="Name">
                        </div>
                        <div class="form-group">
                          <input type="number" name="Price" id="price" tabindex="2" class="form-control" placeholder="Price" >
                        </div>
                        <div class="form-group">
                          <div class="row">
                            <div class="col-sm-6 col-sm-offset-3">
                              <button type="button" class="btn btn-sm btn-primary btn-create">ADD PRODUCT</button>
                            </div>
                          </div>
                        </div>
                    </form>
                    <form id="update-form" role="form" style="display: none;">
                      <h2>UPDATE PRODUCT</h2>
                        <div class="form-group">
                          <input type="text" name="Name" id="name" tabindex="1" class="form-control" placeholder="Name">
                        </div>
                        <div class="form-group">
                          <input type="number" name="Price" id="price" tabindex="2" class="form-control" placeholder="Price">
                        </div>
                        <div class="form-group">
                          <div class="row">
                            <div class="col-sm-6 col-sm-offset-3">
                            </div>
                          </div>
                        </div>
                    </form>
                  </div>
                </div>
              </div>
              <div class="panel-body">
                <table class="table table-striped table-bordered table-list ">
                  <thead>
                    <tr>
                        <th><em class="fa fa-cog"></em></th>
                        <th>ID</th>
                        <th class="hidden-xs">Name</th>
                        <th>Price</th>
                        <th>createdAt</th>
                        <th>updatedAt</th>
                    </tr>
                  </thead>
                  <tbody>
                          <tr>
                            <td align="center">
                              <a class="btn btn-default"><em class="fa fa-pencil"></em></a>
                              <a class="btn btn-danger"><em class="fa fa-trash"></em></a>
                            </td>
                            <td>1</td>
                            <td>kdfnsnf</td>
                            <td>sdfsf</td>
                            <td>sdfsdf</td>
                            <td>dsfssfdsdf</td>
                          </tr>
                        </tbody>
                </table>

              </div>

            </div>

</div>
</div>
</div>
</html>
</template>
<script>
export default {
  name: 'product',
  data () {
    return {
      products: []
      }
    }
  },
  methods: {
   myFunction () {
      var x = document.getElementById('product-form')
      if (x.style.display === 'none') {
        x.style.display = 'block'
      } else {
        x.style.display = 'none'
      }
    },
    myFunction1 () {
      var x = document.getElementById('update-form')
      if (x.style.display === 'none') {
        x.style.display = 'block'
      } else {
        x.style.display = 'none'
      }
    }
}

</script>
<style scoped>
.panel-table .panel-body{
  padding:0;
}

.panel-table .panel-body .table-bordered{
  border-style: none;
  margin:0;
}

.panel-table .panel-body .table-bordered > thead > tr > th:first-of-type {
    text-align:center;
    width: 60px;
}

.panel-table .panel-body .table-bordered > thead > tr > th:last-of-type,
.panel-table .panel-body .table-bordered > tbody > tr > td:last-of-type {
  border-right: 0px;
}

.panel-table .panel-body .table-bordered > thead > tr > th:first-of-type,
.panel-table .panel-body .table-bordered > tbody > tr > td:first-of-type {
  border-left: 0px;
}

.panel-table .panel-body .table-bordered > tbody > tr:first-of-type > td{
  border-bottom: 0px;
}

.panel-table .panel-body .table-bordered > thead > tr:first-of-type > th{
  border-top: 0px;
}

.panel-table .panel-footer .pagination{
  margin:0;
}

/*
used to vertically center elements, may need modification if you're not using default sizes.
*/
.panel-table .panel-footer .col{
 line-height: 34px;
 height: 34px;
}

.panel-table .panel-heading .col h3{
 line-height: 30px;
 height: 30px;
}

.panel-table .panel-body .table-bordered > tbody > tr > td{
  line-height: 34px;
}

</style>
