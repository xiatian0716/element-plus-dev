## TimePicker

Use el Time Picker para input de tipo time.

### Selector de tiempo arbitrario

Un tiempo arbitrario puede ser escogido.

:::demo Al usar el tag `el-time-picker`, es posible limitar el rango de tiempo al especificar `selectableRange`. Por defecto, es posible hacer scroll con la rueda del mouse para escoger el tiempo, alternativamente se pueden utilizar las flechas de control cuando el atributo `arrow-control` esté establecido.

```html
<template>
  <el-time-picker
    v-model="value1"
    :picker-options="{
      selectableRange: '18:30:00 - 20:30:00'
    }"
    placeholder="Arbitrary time">
  </el-time-picker>
  <el-time-picker
    arrow-control
    v-model="value2"
    :picker-options="{
      selectableRange: '18:30:00 - 20:30:00'
    }"
    placeholder="Arbitrary time">
  </el-time-picker>
</template>

<script>
  export default {
    data() {
      return {
        value1: new Date(2016, 9, 10, 18, 40),
        value2: new Date(2016, 9, 10, 18, 40)
      };
    }
  }
</script>
```
:::

### Rango de tiempo arbitrario

Es posible escoger un rango de tiempo arbitrario.

:::demo Es posible seleccionar un rango de tiempo al añadir el atributo `is-range`. También, `arrow-control` es soportado en modo de rango.
```html
<template>
  <el-time-picker
    is-range
    v-model="value1"
    range-separator="To"
    start-placeholder="Start time"
    end-placeholder="End time">
  </el-time-picker>
  <el-time-picker
    is-range
    arrow-control
    v-model="value2"
    range-separator="To"
    start-placeholder="Start time"
    end-placeholder="End time">
  </el-time-picker>
</template>

<script>
  export default {
    data() {
      return {
        value1: [new Date(2016, 9, 10, 8, 40), new Date(2016, 9, 10, 9, 40)],
        value2: [new Date(2016, 9, 10, 8, 40), new Date(2016, 9, 10, 9, 40)]
      };
    }
  }
</script>
```
:::

### Atributos
| Atributo          | Descripción                              | Tipo                                     | Valores aceptados                        | Por defecto          |
| ----------------- | ---------------------------------------- | ---------------------------------------- | ---------------------------------------- | -------------------- |
| value / v-model    | valor enlazado                           | date(TimePicker) / string(TimeSelect)    | -                                        | -                    |
| readonly          | si el Time Picker está en modo de sólo lectura | boolean                                  | —                                        | false                |
| disabled          | si el Time Picker se encuentra deshabilitado | boolean                                  | —                                        | false                |
| editable          | si el input puede ser editado            | boolean                                  | —                                        | true                 |
| clearable         | si mostrar el botón de borrado           | boolean                                  | —                                        | true                 |
| size              | tamaño del input                         | string                                   | medium / small / mini                    | —                    |
| placeholder       | placeholder en un modo fuera de rango    | string                                   | —                                        | —                    |
| start-placeholder | placeholder para el tiempo de inicio en modo de rango | string                                   | —                                        | —                    |
| end-placeholder   | placeholder para el tiempo de finalización en modo de rango | string                                   | —                                        | —                    |
| is-range          | si es posible escoger un rango de tiempo, solo funciona con `<el-time-picker>` | boolean                                  | —                                        | false                |
| arrow-control     | si es posible escoger el tiempo usando los botones de flecha, solo funciona con `<el-time-picker>` | boolean                                  | —                                        | false                |
| align             | alineación                               | left / center / right                    | left                                     |                      |
| popper-class      | nombre de clase personalizada para el dropdown del Time Picker | string                                   | —                                        | —                    |
| range-separator   | separador de rango                       | string                                   | -                                        | '-'                  |
| default-value     | opcional, fecha por defecto del calendario | Fecha para Selector de Tiempo, string para el Seleccionador de Tiempo | cualquier cosa aceptada por `new Date()` para el Selector de Tiempo,  Selector de Tiempo, valor seleccionable para el Seleccionador de Tiempo | —                    |
| name              | como `name` en input nativo              | string                                   | —                                        | —                    |
| prefix-icon       | Clase personalizada para el icono de prefijado | string                                   | —                                        | el-icon-time         |
| clear-icon        | Clase personalizada para el icono `clear` | string                                   | —                                        | el-icon-circle-close |

### Opciones para Time Picker
| Atributo        | Descripción                              | Tipo           | Valores aceptados                   | Por defecto |
| --------------- | ---------------------------------------- | -------------- | ----------------------------------- | ----------- |
| selectableRange | rango de tiempo disponible p.ej. `'18:30:00 - 20:30:00'`ó`['09:30:00 - 12:00:00', '14:30:00 - 18:30:00']` | string / array | —                                   | —           |
| format          | formato para el selector                 | string         | hour `HH`, minute `mm`, second `ss` | HH:mm:ss    |


### Eventos
| Nombre de Evento | Descripción                              | Parámetros                     |
| ---------------- | ---------------------------------------- | ------------------------------ |
| change           | se lanza cuando el usuario confirma el valor | valor vinculado del componente |
| blur             | se lanza cuando el input se difumina     | instancia del componente       |
| focus            | se lanza cuando el input se enfoca       | instancia del componente       |

### Metodos
| Metodo | Descripción                | Parameteros |
| ------ | -------------------------- | ----------- |
| focus  | coloca el foco en el input | —           |
