a = 1.9;
b = 1;
c = 0.8;
d = 1;
f = 1;

x = linspace(0.01, 2*pi, 1000);

f_x = sin(b*x) ./ x;
g_x = c * exp(-d*x) .* cos(f*x);

 
figure;
plot(x, f_x, 'b', 'LineWidth', 2);
title('График f(x)');
xlabel('x');
ylabel('f(x)');
grid on;

figure;
plot(x, g_x, 'r', 'LineWidth', 2);
title('График g(x)');
xlabel('x');
ylabel('g(x)');
grid on;

 
figure;
hold on;
plot(x, f_x, 'b', 'LineWidth', 2);
plot(x, g_x, 'r--', 'LineWidth', 2);
title('Графики f(x) и g(x)');
xlabel('x');
ylabel('y');
legend('f(x)', 'g(x)');
grid on;
hold off;

a = 1.9;
b = 1;
c = 0.8;

[x, y] = meshgrid(linspace(-1, 1, 100));

z = (sin(a * x.^2 + cos(y))).^2;

 
figure;

subplot(1, 2, 1);
contourf(x, y, z, 20);  
title('Контурный график функции z(x, y)');
xlabel('x');
ylabel('y');
colorbar;
grid on;

subplot(1, 2, 2);
mesh(x, y, z);  
title('3D график функции z(x, y)');
xlabel('x');
ylabel('y');
zlabel('z');
grid on;
 
figure;
subplot(2, 1, 1);
plot(x, f_x, 'b', 'LineWidth', 2);
title('График f(x)');
xlabel('x');
ylabel('f(x)');
grid on;

subplot(2, 1, 2);
plot(x, g_x, 'r--', 'LineWidth', 2);
title('График g(x)');
xlabel('x');
ylabel('g(x)');
grid on;
