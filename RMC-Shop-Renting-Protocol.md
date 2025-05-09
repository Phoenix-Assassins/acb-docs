A custom Hermes RMC service for business investment management in singleplayer mode.

The definitions come from MacOS version of the game.

| Method ID | Method Name |
|-----------|-------------|
| 1 | [GetShopRentingStat](#1-getshoprentingstat) |
| 2 | [RentShop](#2-rentshop) |
| 3 | [GetAllShopRentingStats](#3-getallshoprentingstats) |

# (1) GetShopRentingStat

## Request

| Type | Name |
|------|------|
| Uint32 | shopID |

## Response

| Type | Name |
|------|------|
| [ShopRentingStat](#shoprentingstat-structure) | shopRentingStat |

# (2) RentShop

This method is not implemented by the Windows version.

## Request

| Type | Name |
|------|------|
| Uint32 | shopID |

## Response

This method does not return anything.

# (3) GetAllShopRentingStats

## Request

This method does not take any parameters.

## Response

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[ShopRentingStat](#shoprentingstat-structure)> | shopRentingStats |

# Types

## ShopRentingStat ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| Uint32 | m_shopID |
| Float | m_currentRenterPercentage |
| Float | m_allTimeRenterPercentage |
| Uint32 | m_price |
| Int8 | m_shopRegion |
