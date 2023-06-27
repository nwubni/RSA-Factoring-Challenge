#!/usr/bin/python3

import sys


def factorize(number):
    factors = [0, 0]

    if number % 2 == 0:
        factors[0] = number // 2
        factors[1] = 2

    for i in range(3, int(number**0.5) + 1, 2):
        if number % i == 0:
            factors[0] = number // i
            factors[1] = i
            break

    return factors


def main():
    if len(sys.argv) != 2:
        print("Usage: factors <file>")
        return

    filename = sys.argv[1]

    try:
        with open(filename, 'r') as file:
            numbers = file.readlines()
            for number in numbers:
                number = int(number.strip())
                factors = factorize(number)
                print(f"{number}={factors[0]}*{factors[1]}")
    except FileNotFoundError:
        print(f"File '{filename}' not found.")


if __name__ == "__main__":
    main()
