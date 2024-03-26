![image](https://github.com/Adalab/bda-modulo-1-evaluacion-final-vanediar/assets/157760333/ba988821-1622-4950-9d99-f153e2407b6a)

El código presentado en este repositorio sirve para gestionar el funcionamiento de tiendas online, de una forma sencilla a través de tres bloques principales: inventario, clientes y ventas. 

Con estos tres bloques podrás gestionar cualquier tipo de requerimiento de tu tienda online: 

    - Controlar todo el stock: unidades disponibles, precio, actualizaciones.
    
    - Gestionar todo lo referente a los clientes: registro de clientes, resgistro de sus compras.
    
    - Conocerás el número total de ventas: por cliente, por producto.

A continuación puedes ver una muestra del tipo de código que se usa, en este caso para agregar un producto al inventario:

    def agregar_producto(self, nombre, precio, cantidad):
          producto = {'nombre':nombre, 'precio':precio, 'cantidad':cantidad}
        
          if producto not in self.inventario:
        
              self.inventario.append(producto)
            
              return self.inventario
            
          elif producto['cantidad'] != self.inventario['cantidad']:
        
              self.inventario['cantidad'] = cantidad
            
              return f'Se ha actualizado la cantidad del producto', nombre
            
          else:
        
              print('El producto', nombre, 'ya existe en el inventario')
