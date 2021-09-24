import multiprocessing as mp
import time

def calc_cuad(numeros, result):
    for idx, n in enumerate(numeros):
        result[idx] = n * n #¿esto funciona si ya vimos que no?
        
    print("Resultado del proceso:", result[:])    

nums = range(10)

t = time.time()
result = mp.Array('i', 10)
p1 = mp.Process(target=calc_cuad, args=(nums,result))

p1.start()
p1.join()

print("Resultado fuera del proceso:", result[:]) # ¿vamos a poder ver el contenido de result?

print("Tiempo de ejecución: ", time.time()-t)
print("Finaliza ejecución")
