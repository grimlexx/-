1. 

C = input('Введите элементы массива C: ');

min_element = min(C);

ind = find(C > 0);
[~, min_index] = min(C(ind));

fprintf('Минимальный элемент: %.2f\n', min_element);
fprintf('Порядковый номер среди положительных элементов: %d\n', ind(min_index));

2.
 a = 1.9;
b = 1;
c = 0.8;
d = 1;
f = 1;

x = linspace(0.01, 2*pi, 1000);

f_x = sin(b*x) ./ x;
g_x = c * exp(-d*x) .* cos(f*x);

figure;
subplot(2, 1, 1);
plot(x, f_x, 'b', 'LineWidth', 2);
title('График f(x)');
xlabel('x');
ylabel('f(x)');

subplot(2, 1, 2);
plot(x, g_x, 'r', 'LineWidth', 2);
title('График g(x)');
xlabel('x');
ylabel('g(x)');

legend('f(x)', 'g(x)');

grid on;

3
a = 1.9;
b = 1;
c = 0.8;

[x, y] = meshgrid(linspace(-1, 1, 100));

z = (sin(a * x.^2 + cos(y))).^2;


figure;
surf(x, y, z);
title('График функции z(x, y)');
xlabel('x');
ylabel('y');
zlabel('z');

grid on;

4.

S = [50, 45, 51, 55, 79, 90, 110, 100, 92, 76, 79, 88];

figure;
bar(S);
title('Средние доходности по месяцам');
xlabel('Месяц');
ylabel('Доходность');

 
figure;
pie(S);
title('Модельное распределение');
legend('Январь', 'Февраль', 'Март', 'Апрель', 'Май', 'Июнь', 'Июль', 'Август', 'Сентябрь', 'Октябрь', 'Ноябрь', 'Декабрь');
