---
title: "Opcodes"
---

# ¿Que son los "Opcodes"?
?

## https://www.evm.codes/
Página que explica cada código binario de la "Ethereum Virtual Machine".

## https://www.evm.codes/playground
- Simulación de EVM
- Se debe elegir la opción "Bytecode"

## Ejemplo
Código: 363d3d37363df3

Buenas noches, les comparto mi solución al reto de la 3ra semana:
- [**36: CALLDATASIZE**] Obtiene el tamaño de los datos ingresados. Como no hay datos, retorna cero en el stack.
- [**3D: RETURNDATASIZE**] Obtiene el tamaño de los datos de salida. Como el anterior fue cero, también se retornará cero. Este opcode se repite y seguirá retornando cero.
- [**37: CALLDATACOPY**] Copia los datos de la llamada anterior. Como los anteriores datos eran cero, se retornará un valor vacío.
- [**36: CALLDATASIZE**] El tamaño de los datos sigue siendo cero. Por lo que retornará cero.
- [**3D: RETURNDATASIZE**] El tamaño de los datos de salida seguirá siendo cero. Por lo que se agrega otro cero al stack.
- [**F3: RETURN**] Termina la ejecución y retorna los datos. Finalmente se vací el stack.


### 36
CALLDATASIZE. Get size of input data in current environment. minimun gas.
Stack output 
`size`: byte size of the calldata

### 3d
RETURNDATASIZE. Get size of output data from the previous call from the current environment
Stack output
`size`: byte size of the return data from the last executed sub context.

### 37
CALLDATACOPY. Copy input data in current environment to memory
Stack input
1.  `destOffset`: byte offset in the [memory](https://www.evm.codes/about) where the result will be copied.
2.  `offset`: byte offset in the [calldata](https://www.evm.codes/about) to copy.
3.  `size`: byte size to copy.

### f3
RETURN. Halt execution returning output data.
Stack input
1.  `offset`: byte offset in the [memory](https://www.evm.codes/about) in bytes, to copy what will be the [return data](https://www.evm.codes/about) of this [context](https://www.evm.codes/about).
2.  `size`: byte size to copy (size of the [return data](https://www.evm.codes/about)).