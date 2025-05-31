def precio():
    print("cual es el precio del producto")
    preciof=float(input())
    return preciof

def calculos(porcentaje,valor):
    porc=porcentaje*valor
    return porc
def procesar(preciof):
    ganancia=calculos(0.25,preciof)
    comision=calculos(0.20,preciof)
    precio_base=preciof+ganancia+comision
    iva=calculos(precio_base,0.16)
    precio_venta=precio_base+iva
    return precio_base, precio_venta,iva

preciof=precio()
precio_base, precio_venta,iva=procesar(preciof)

def factura(precio_base,precio_venta,iva):
    print(f"el iva es {iva}%")
    print(f"precio base es de {precio_base}$")
    print(f"precio final es de {precio_venta}$")

factura(precio_base,precio_venta,iva) 
