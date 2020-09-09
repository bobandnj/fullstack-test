# Nathan James Full Stack Developer - Work Sample

A PHP project to integrate with the external ordering system and external warehouse system using REST API.

## Background of the task

This integration is the first step towards a full integration with multiple warehouses and ordering systems. We would like to support integration with multiple external systems and to be able to collect warehouse items and orders several times per day.

## Requirements

The goal of the work sample is to create an integration with WAREHOUSE_X warehouse system and ORDERING_Y ordering system.

We should fetch all orders with status "new" from the API. If the order is valid, update the order status to "processed". If the order is not valid, the order status should be to "failed".

The order is valid if order items quantities are satisfied with warehouse items quantity and if our warehouse items are available (`availableFromDate`) before the planned order shipping date (`shippingDate`).

## External systems

### External warehouse system (WAREHOUSE_X)

The external warehouse system has provided us with the following publicly available endpoint:

1) GET https://5f591c568040620016ab8de2.mockapi.io/api/v1/warehouse-items

### External ordering system (ORDERING_Y)

The external ordering system has provided us with the following publicly available endpoints:

1) GET https://5f591c568040620016ab8de2.mockapi.io/api/v1/orders
2) PUT https://5f591c568040620016ab8de2.mockapi.io/api/v1/orders/:orderId
