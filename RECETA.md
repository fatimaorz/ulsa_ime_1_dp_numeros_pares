# Receta: Guardar los números pares

1. Mostrar mensaje de bienvenida
2. cANTIDAD ←
2. totalPares ← 0
3. contador ← 0
4. PARA contador < CANTIDAD HACER
       numero ← leerEntero("Escribe un numero:")
       SI numero (n MOD2=0) ENTONCES
           pares[totalPares] ← numero
           totalPares ← totalPares+1
       FIN SI
       contador ← contador + 1
   FIN PARA
5. Mostrar "Pares encontrados: " y totalPares
6. i ← 0
7. PARA i < totalPares HACER
       Mostrar pares[i]
       i ← i + 1
   FIN PARA