# 代码问题

请查看以下 PHP 代码，并找出潜在的 bug 或改进之处：

```php
public function calculateDiscount($price, $discount) {
    if ($discount > 100) {
        return "Discount cannot be greater than 100%";
    }
    
    $finalPrice = $price - ($price * ($discount / 100));
    
    if ($finalPrice < 0) {
        return 0; // Ensure the final price is not negative
    }
    
    return $finalPrice;
}
