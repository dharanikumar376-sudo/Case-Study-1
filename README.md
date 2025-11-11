
#include <iostream>
#include <vector>
#include <string>
using namespace std;
class ShoppingCart {
private:
 vector<string> items;
public:
 // Default constructor
 ShoppingCart() {
 cout << "Empty cart created." << endl;
 }
 // Parameterized constructor
 ShoppingCart(vector<string> initialItems) {
 items = initialItems;
 cout << "Cart initialized with items." << endl;
 }
 // Copy constructor
 ShoppingCart(const ShoppingCart &cart) {
 items = cart.items;
 cout << "Cart copied for backup." << endl;
 }
 // Add item to cart
 void addItem(string item) {
 items.push_back(item);
 }
 // Display cart items
 void display() {
 cout << "Cart items: ";
 for (string item : items) {
 cout << item << " ";
 }
 cout << endl;
 }
};
int main() {
 // Using default constructor
 ShoppingCart cart1;
 cart1.addItem("Laptop");
 cart1.addItem("Mouse");
 cart1.display();
// Using parameterized constructor
 vector<string> initialItems = {"Keyboard", "Monitor"};
 ShoppingCart cart2(initialItems);
 cart2.display();
 // Using copy constructor
 ShoppingCart cart3(cart2);
 cart3.addItem("USB Drive");
 cart3.display();
 return 0;
}
