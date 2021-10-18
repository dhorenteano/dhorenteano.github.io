var app = angular.module('myModule', [])
                .controller('myController', function($scope){
                $scope.carts=[];
                $scope.products = [
                    {id: "1", name: "Hes Into Her", image: "assets/maxxx.png", price: 850},
                    {id: "2", name: "Baka Sakali Trilogy", image: "assets/2.jpg", price: 500},
                    {id: "3", name: "The Four Bad Boys And Me", image: "assets/3.jpg", price: 250},
                    {id: "4", name: "Montello High", image: "assets/4.jpg", price: 200},
                    {id: "5", name: "Defend Me Attorney", image: "assets/5.jpg", price: 500},
                    {id: "6", name: "A and D", image: "assets/6.jpg", price: 190},
                    {id: "7", name: "AFGITMOLFM", image: "assets/7.jpg", price: 500},
                    {id: "8", name: "Black Equation", image: "assets/8.jpg", price: 190},
                    {id: "9", name: "Costa Leona Series (3-6)", image: "assets/9.jpg", price: 3800},
                    {id: "10", name: "Heartless", image: "assets/10.jpg", price: 260},
                    {id: "11", name: "Fearless Queen", image: "assets/111.jpg", price: 400},
                    {id: "12", name: "The Ten Year Gap", image: "assets/123.jpg", price: 80},

                ];
                
                $scope.add_cart = function(product){
                    if(product){
                        $scope.carts.push({id: product.id, name: product.name, price: product.price});
                    }   
                }
                        
                    
                $scope.total = 0;
                
                $scope.setTotals = function(cart){
                    if(cart){
                        $scope.total += cart.price;
                    }
                }
                
                $scope.remove_cart = function(cart){
                    if(cart){
                        $scope.carts.splice($scope.carts.indexOf(cart), 1);
                        $scope.total -= cart.price;
                    }
                }
    });