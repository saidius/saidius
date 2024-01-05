- 👋 Hi, I’m @saidius
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

- My telegram
-   t.me/m1zhark
    My VK
-      https://vk.com/reggvenny
   My Discord 
-      @furrersaidius

<!---
saidius/saidius is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

#include <iostream>
#include <vector>

class Gift {
public:
    Gift(const std::string& name, double price) : name(name), price(price) {}

    void display() const {
        std::cout << "Gift: " << name << ", Price: $" << price << std::endl;
    }

private:
    std::string name;
    double price;
};

class GiftShop {
public:
    GiftShop(const std::string& shopName) : shopName(shopName) {}

    void addGift(const Gift& gift) {
        gifts.push_back(gift);
    }

    void displayInventory() const {
        std::cout << "Welcome to " << shopName << " Gift Shop!\n";
        std::cout << "Inventory:\n";
        for (const auto& gift : gifts) {
            gift.display();
        }
    }

private:
    std::string shopName;
    std::vector<Gift> gifts;
};

int main() {
    GiftShop myGiftShop("C++ Gift Emporium");

    Gift mug("C++ Logo Mug", 15.99);
    Gift book("C++ Programming Guide", 29.99);
    Gift plush("C++ Code Plush Toy", 12.99);

    myGiftShop.addGift(mug);
    myGiftShop.addGift(book);
    myGiftShop.addGift(plush);

    myGiftShop.displayInventory();

    return 0;
}
