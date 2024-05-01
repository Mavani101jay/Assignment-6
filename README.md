# Assignment-6

x = [1.27 0.943 0.8488 0.7489 0.7489 0.6882 0.670 0.652 0.6882];
y = [39 40.75 42 43.25 44 45 45.25 45.75 46];
p = polyfit(x, y, 2);
x_curve = linspace(min(x), max(x), 100);
y_curve = polyval(p, x_curve);
scatter(x, y, 'r'); 
hold on;
plot(x_curve, y_curve, 'b-');
xlabel('x');
ylabel('y');
title('Parabolic Curve Fitting');
legend('Data Points', 'Parabolic Curve');
hold off;
