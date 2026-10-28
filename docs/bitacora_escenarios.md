# Bitácora de Escenarios

```text
E01 O001: OK   | evaluar_descuento -> 10%. Estado final: DRAFT | eventos=(ninguno)
E02 O002: OK   | evaluar_descuento -> 0%. Estado final: DRAFT | eventos=(ninguno)
E03 O003: OK   | confirm() -> InvalidOrderData: Requiere artículos y cliente activo para confirmarse. Estado final: DRAFT | eventos=(ninguno)
E04 O005: OK   | evaluar_descuento -> 0%. Estado final: DRAFT | eventos=(ninguno)
E05 O006: OK   | evaluar_descuento -> 5%. Estado final: DRAFT | eventos=(ninguno)
E06 O007: OK   | confirm() -> InvalidOrderData: Requiere artículos y cliente activo para confirmarse. Estado final: DRAFT | eventos=(ninguno)
E07 O008: OK   | confirm() -> OK. Estado final: CONFIRMED | eventos=OrderConfirmed
E08 O009: OK   | add_item(SKU003 x2) -> OrderItemLimitExceeded: Máximo 20 unidades. Estado final: DRAFT | eventos=(ninguno)
E09 O010: OK   | evaluar_descuento -> 0%. Estado final: DRAFT | eventos=(ninguno)
E10 O011: OK   | evaluar_descuento -> 0%. Estado final: DRAFT | eventos=(ninguno)
E11 O012: OK   | confirm() -> OK; ship('') -> InvalidOrderData: El envío requiere un número de guía. Estado final: CONFIRMED | eventos=OrderConfirmed
E12 O013: OK   | confirm() -> OK; confirm() (2a vez) -> InvalidOrderTransition: Solo se puede confirmar un pedido DRAFT. Estado final: CONFIRMED | eventos=OrderConfirmed
E13 O014: OK   | confirm()-> OK; ship('GUIA-014')-> OK; cancel('Ya no lo quiero') -> InvalidOrderTransition: Solo se puede cancelar un pedido CONFIRMED. Estado final: SHIPPED | eventos=OrderConfirmed, OrderShipped
E14 O015: OK   | confirm()-> OK; ship('GUIA-015')-> OK; return_order() -> OK. Estado final: RETURNED | eventos=OrderConfirmed, OrderShipped, OrderReturned
E15 O016: OK   | confirm()-> OK; ship('GUIA-016')-> OK; deliver() -> OK. Estado final: DELIVERED | eventos=OrderConfirmed, OrderShipped, OrderDelivered
```
