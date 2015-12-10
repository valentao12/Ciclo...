# Ciclo...
project
ventas=[2000 5000 100 800 300 1000 2200 350 50 1300]; % vector de ventas
i=1; % se encargará de recorrer todas las posiciones del vector ventas
while(i <= length (ventas)) % length(ventas) = 10 ya que el vector tiene 10 elementos.
 if(ventas(i)<=400)
 comisiones(i)=ventas(i).*0.01;
 elseif(ventas(i)>400 && ventas(i)<1000)
 comisiones(i)=ventas(i).*0.03;
 else
 comisiones(i)=ventas(i).*0.05;
 end
 i=i+1;
End
% creamos la tabla a graficar
tabla=[ventas' comisiones'];
disp('las comisiones por venta son: ');
disp(tabla);
plot(ventas , comisiones, ‘b*’)
