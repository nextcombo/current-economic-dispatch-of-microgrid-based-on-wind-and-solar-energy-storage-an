# Current Economic Dispatch of Microgrid Based on Wind and Solar Energy Storage and Demand Response (Matlab Code Implementation)

Microgrid Economic Dispatch Based on Wind and Solar Energy Storage and Demand Response (Matlab Code Implementation)
Partial code:
% Unmet load percentage\nP3 = Pload1 - P1;\nCOST1 = P3(P3 > 0);\nif ~isempty(COST1)\n    fprintf('Unmet load share%f :\n', mean(COST1) / max(Pload1));\n    fprintf('Unsatisfied total load%f :\n', sum(COST1));\nelse\n    fprintf('Unmet load percentage%f :\n', 0);\n    fprintf('Unsatisfied total load%f :\n', 0);\nend\n\n% Drawing 1: Comparative output of various parts\nfigure('Color','white');\nplot(1:24, Pload1, 'rd--', 'LineWidth',2, 'MarkerSize',6, 'DisplayName','Load');\nhold on;\nplot(1:24, bestX(1,:), 'b+-.' , 'LineWidth',2, 'MarkerSize',6, 'DisplayName','True power output of the fan');\nplot(1:24, bestX(2,:), 'kx--' , 'LineWidth',2, 'MarkerSize',6, 'DisplayName','Photovoltaic real power output');\nplot(1:24, bestX(3,:), 'ms--', 'LineWidth',2, 'MarkerSize',6, 'DisplayName','Main network output');\nplot(1:24, bestX(4,:), 'c--' , 'LineWidth',2, 'MarkerSize',6, 'DisplayName','Energy storage output');\nplot(1:24, Pload1 - bestX(1,:) - bestX(2,:) - bestX(3,:) - bestX(4,:) - bestX(5,:), ...\n     'yv--', 'LineWidth',2, 'MarkerSize',6, 'DisplayName','Unsatisfied load');\nxlabel('t/hour', 'FontSize',18);\nylabel('Electricity consumption/kWh', 'FontSize',18);\nxticks(1:24);\nlegend('Location','best');\ngrid on;\n\n% Plot 2: Load comparison before and after demand response\nfigure('Color','white');\nplot(1:24, Pload1, 'rd--', 'LineWidth',2, 'MarkerSize',6, 'DisplayName','DRFront load');\nhold on;\nplot(1:24, Pload1 - bestX(5,:), 'yv--', 'LineWidth',2, 'MarkerSize',6, 'DisplayName','DRPost-load');\nxlabel('t/hour', 'FontSize',18);\nylabel('Electricity consumption/kWh', 'FontSize',18);\nxticks(1:24);\nlegend('Location','best');\ngrid on;\n\n  

## Images

![Microgrid Economic Dispatch Based on Wind and Solar Energy Storage and Demand Response (Matlab Code Implementation)](cover.jpg)

<!-- PAYMENT_BLOCK -->

## Get this dataset

- Payment link (Stripe): [Buy now](https://buy.stripe.com/3cs8yP7sY87d0vu9AB)
- Payment QR code: ![Payment QR code](pay.png)

<!-- /PAYMENT_BLOCK -->
