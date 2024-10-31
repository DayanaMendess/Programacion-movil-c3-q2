# Componente 1

```js 
<!-- Contenido principal -->
    <ion-content :fullscreen="true" class="content-container">

```
# Componente 2
 ```js     
      <!-- Barra de búsqueda -->
      <ion-searchbar class="spaced-item" color="primary" placeholder="Buscar"></ion-searchbar>
```
# Componente 3
```js
      <!-- Entrada de usuario -->
      <ion-input class="spaced-item" label="Usuario" label-placement="floating" fill="solid" placeholder="Ingrese usuario"></ion-input>
```
# Componente 4
```js
      <!-- Entrada de contraseña -->
      <ion-input class="spaced-item" label="Contraseña" label-placement="floating" fill="outline" placeholder="Ingrese contraseña"></ion-input>
```
# Componente 5
```js
      <!-- Selección de género -->
      <ion-list class="spaced-item">
        <ion-item>
          <ion-select placeholder="Seleccione un Género">
            <div slot="label">Género <ion-text color="danger">*</ion-text></div>
            <ion-select-option value="Masculino">Masculino</ion-select-option>
            <ion-select-option value="Femenino">Femenino</ion-select-option>
          </ion-select>
        </ion-item>
      </ion-list>
```
# Componente 6 
```js
      <!-- Checkbox de acceso -->
      <ion-item class="spaced-item">
        <ion-checkbox slot="start" aria-label="Acceder"></ion-checkbox>
        <ion-label>Acceder</ion-label>
      </ion-item>

      <!-- Sección del menú -->
      <ion-toolbar class="menu-section">
        <ion-buttons slot="start">
          <ion-menu-button :auto-hide="false"></ion-menu-button>
        </ion-buttons>
        <ion-title>Menú</ion-title>
      </ion-toolbar>
```
# Componente 7
```js
      <!-- Tarjeta de Notificaciones -->
<ion-card class="spaced-item">
  <ion-card-header>
    <ion-card-title>Notificación</ion-card-title>
    <ion-card-subtitle>Importante</ion-card-subtitle>
  </ion-card-header>
  <ion-card-content>
    Recuerda revisar las actividades pendientes para esta semana. Mantente al día con tus asignaciones.
  </ion-card-content>
</ion-card>
```
# Componente 8
```js
<!-- Listado de Mensajes Recientes -->
<ion-list class="content-subsection spaced-item">
  <ion-item>
    <ion-icon name="mail-outline" slot="start"></ion-icon>
    <ion-label>
      <h2>Mensaje de Profesor</h2>
      <p>Revisa la nueva asignación en Programación.</p>
    </ion-label>
  </ion-item>
  <ion-item>
    <ion-icon name="mail-outline" slot="start"></ion-icon>
    <ion-label>
      <h2>Recordatorio</h2>
      <p>Entrega el proyecto final el próximo lunes.</p>
    </ion-label>
  </ion-item>
  <ion-item>
    <ion-icon name="mail-outline" slot="start"></ion-icon>
    <ion-label>
      <h2>Notificación del Sistema</h2>
      <p>Se actualizaron las políticas de uso.</p>
    </ion-label>
  </ion-item>
</ion-list>
```
# Componente 9
```js


      <!-- Información de materias (Seleccionable con checkboxes y sin espacio extra) -->
      <ion-list class="content-subsection" style="margin-bottom: 8px;">
        <ion-item>
          <ion-checkbox slot="start" aria-label="Materia"></ion-checkbox>
          <ion-label>Materia</ion-label>
        </ion-item>
        <ion-item>
          <ion-checkbox slot="start" aria-label="Horario"></ion-checkbox>
          <ion-label>Horario</ion-label>
        </ion-item>
        <ion-item>
          <ion-checkbox slot="start" aria-label="Actividades"></ion-checkbox>
          <ion-label>Actividades</ion-label>
        </ion-item>
        <ion-item>
          <ion-checkbox slot="start" aria-label="Calificaciones"></ion-checkbox>
          <ion-label>Calificaciones</ion-label>
        </ion-item>
      </ion-list>
      
```
# Componente 10 
```js
      <!-- Sección de materias -->
      <ion-header>
        <ion-toolbar>
          <ion-title>Materias</ion-title>
        </ion-toolbar>
      </ion-header>
      <ion-content color="light" class="content-subsection">
        <ion-list :inset="true">
          <ion-item>
            <ion-checkbox slot="start" aria-label="Toggle task completion"></ion-checkbox>
            <ion-input aria-label="Task name" value="Programación"></ion-input>
          </ion-item>
          <ion-item>
            <ion-checkbox slot="start" aria-label="Toggle task completion"></ion-checkbox>
            <ion-input aria-label="Task name" value="Electrónica"></ion-input>
          </ion-item>
          <ion-item>
            <ion-checkbox slot="start" aria-label="Toggle task completion"></ion-checkbox>
            <ion-input aria-label="Task name" value="Diseño Sistemas"></ion-input>
          </ion-item>
          <ion-item>
            <ion-checkbox slot="start" aria-label="Toggle task completion"></ion-checkbox>
            <ion-input aria-label="Task name" value="Base Datos"></ion-input>
          </ion-item>
        </ion-list>
      </ion-content>
    </ion-content>
  </ion-page>
</template>
```