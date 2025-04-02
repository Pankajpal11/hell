def product_of_digits(arr):
    result = []
    for num in arr:
        if num == 0:
            result.append(0)
            continue

        num = abs(num)
        product = 1
        while num > 0:
            product *= num % 10
            num //= 10

        result.append(product)

    return result

num = [23,45,102,-37,0]
print(product_of_digits(num))
