# 09/08/2017

**Fotos ayudantia**

### Variables de decisión.

se pueden manipular

### Función objetivo.

pretendemos maximizar o minimizar. Debe tener variables y es un escalar.

### Dominio.

- Relacion entre Variables. poner en la prueba.
- Acota las Variables. poner en la pruebinha.
- De conjunto. poner en la prueba + puntos nota 7.

# Problema 1

### Variables:

x1: cantidad de dinero que le prestamos a cada cliente Personal (en millones de dolares)
x2: cantidad de dinero que le prestamos a cada cliente Automotriz (en millones de dolares)
x3: cantidad de dinero que le prestamos a cada cliente Vivienda (en millones de dolares)
x4: cantidad de dinero que le prestamos a cada cliente Agricola (en millones de dolares)
x5: cantidad de dinero que le prestamos a cada cliente Comercial (en millones de dolares)

### Funcion objetivo

Maximizar utilidad, que es la diferencia entre lo ganado (por el interes) menos lo no recuperado.

ganado: cantidad(probabilidad_pago·interes-probabilidad_no_pago)

lo ganado por Personal: x1(0.9·0.14-0.1)
lo ganado por Automotriz: x2(0.93·0.13-0.07)
...

finalmente, hay que maximizar:

**0.026*x1+0.0509*x2+0.0864*x3+0.06875*x4+0.078*x5**

#### Restricciones:

**poner descripcion a cada restrccion en prueba**

x1+x2+x3+x4+x5 <= cantidad que tiene el banco = US$12 M = 12

x4+x5 = 40% del fondo = 0.4·12

x3 >= 0.5(x1+x2+x3)

cantidad total no recuperada <= 4%, por lo tanto:
0.1·x1+0.07·x2+0.03·x3+0.05·x4+0.02·x5 <= 0.04(Sumatoria(xi))

### Dominio
**En la prueba +2 decimas**
Naturaleza variable
xi >= 0 para todo i=1,2,...,5

# Problema 2

### Variables

X_i,j = Toneladas de uva que se transportan del viñedo i = {1,2} a la bodega j = {1,2}

### Funcion objetivo

Minimizar 150(distancia_viñedo1_bodega1·X_1,1 + distancia_viñedo1_bodega2·X_1,2+ ...)

= 150(48·X_1,1 + 34·X_1,2 + 41·X_2,1 + 36·X_2,2)

**ojo**: **NO!** se puede hacer una variable **D_i,j = distancia viñedo_i bodega_j** y hacer una sumatoria de D_i,j*X_i,j puesto que esto no seria lineal. si me piden que sea lineal esto no se puede hacer, si no, si se puede.

#### Restricciones

Restricciones de extracción a viñedos:
X_1,1 + X_1,2 <= 400
X_2,1 + X_2,2 <= 400

Capacidad de produccion en bodega:
X_1,1 + X_2,1 <= 480
X_1,2 + X_2,2 <= 600

Procesamiento minimo
X_1,1 + X_1,2 + X_2,1 + X_2,2 >= 600

### Dominio
Naturaleza Variable:
X_i,j >= 0 para todo (i, j) in {1,2} x {1,2}

# Problema 3

### Variables
P_i = numero de ciclos de producción del proceso i = 1, 2, 3

### Funcion objetivo

Maximizar: ganancia - costo
Maximizar: (38(4·P_1 + P_2 + 3·P_3) + 33(3·P_1 + P_2 + 4·P_3)) - (51·P_1 + 11·P_2 + 40·P_3)
Maximizar: 200·P_1 + 60·P_2 + 206·P_3

#### Restricciones

cantidad de barriles A <= 8 millones
3·P_1 + P_2 + 5·P_3 <= 8 · 10^6

cantidad de barriles B <= 5 millones
5·P_1 + P_2 + 3·P_3 <= 5 · 10^6

### Dominio
Naturaleza Variables
P_i >= 0, pertenecen a los naturales, con i = 1, 2, 3
