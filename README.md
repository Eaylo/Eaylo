import UIKit

// Modèle de données pour représenter un restaurant
struct Restaurant {
    let name: String
    let cuisineType: String
    let distance: Double
}

// Vue contrôleur principal pour afficher la liste des restaurants
class RestaurantListViewController: UIViewController {
    
    var restaurants: [Restaurant] = [] // Liste des restaurants
    
    override func viewDidLoad() {
        super.viewDidLoad()
        // Charger les données des restaurants (simulation)
        loadRestaurantData()
        // Afficher la liste des restaurants
        displayRestaurants()
    }
    
    func loadRestaurantData() {
        // Simulation de chargement des données
        restaurants = [
            Restaurant(name: "Restaurant A", cuisineType: "Italian", distance: 1.2),
            Restaurant(name: "Restaurant B", cuisineType: "Japanese", distance: 0.8),
            Restaurant(name: "Restaurant C", cuisineType: "Mexican", distance: 2.5)
        ]
    }
    
    func displayRestaurants() {
        // Afficher les restaurants dans la vue
        for restaurant in restaurants {
            print("Name: \(restaurant.name), Cuisine: \(restaurant.cuisineType), Distance: \(restaurant.distance) km")
        }
    }
}

// Exemple d'utilisation
let restaurantListVC = RestaurantListViewController()
restaurantListVC.viewDidLoad()
