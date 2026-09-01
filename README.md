# Plan Alberto · Registro diario

App web (PWA) de registro diario para un plan de superavit ligero con techo de +3 kg.

Misma base de codigo que las demas apps de clientes: todo lo especifico vive en el objeto
DEFAULT_PLAN al principio del script de index.html.

## Especifico de este plan

- Objetivos: 3.200 kcal en dia de entreno (L-M-X-J) y 2.900 en descanso.
- Control de peso: media de 7 dias, ritmo semanal y aviso al pasar de 0,3 kg/semana o al llegar al techo.
- Dos horarios seleccionables cada dia. En el horario B (entreno a menos de 1 h de comer) la app
  retira sola el AOVE de la comida.
- Objetivo de pasos: 8.000.
- Categoria de vegetales con aporte despreciable: no computa en el total.

## Aviso importante si se anaden mas clientes

localStorage es por dominio, no por carpeta. Cada plan DEBE declarar su propia clave en
`almacen` o un cliente sobrescribiria los datos de otro.
