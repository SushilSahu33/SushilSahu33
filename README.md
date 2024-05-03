
import random
import time

def time_per_second_chance(chance):
    start_time = time.time()
    count = 0
    while True:
        count += 1
        if random.random() < chance:
            break
    end_time = time.time()
    time_taken = end_time - start_time
    return time_taken / count

chance = float(input("Enter the chance of occurrence (between 0 and 1): "))
if chance < 0 or chance > 1:
    print("Invalid chance value. Please enter a value between 0 and 1.")
else:
    time_per_second = time_per_second_chance(chance)
    print("Time per second chance of occurrence:", time_per_second, "seconds"
