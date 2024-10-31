```js 
<!-- Componente CRUD -->
        <ion-card class="crud-card section">
          <ion-card-header>
            <ion-card-title>Gestión de Elementos</ion-card-title>
          </ion-card-header>
          <ion-card-content>
            <ion-button @click="createItem" color="success">Crear</ion-button>
            <ion-button @click="readItem" color="primary">Leer</ion-button>
            <ion-button @click="updateItem" color="warning">Actualizar</ion-button>
            <ion-button @click="deleteItem" color="danger">Eliminar</ion-button>
          </ion-card-content>
        </ion-card>
        
```
  # componente 2
```js 
        <!-- Componente de Formulario de Registro -->
        <ion-card class="form-card section">
          <ion-card-header>
            <ion-card-title>Formulario de Registro</ion-card-title>
          </ion-card-header>
          <ion-card-content>
            <ion-input placeholder="Nombre" label="Nombre" label-placement="floating" fill="solid"></ion-input>
            <ion-input placeholder="Correo" label="Correo" label-placement="floating" fill="solid"></ion-input>
            <ion-input placeholder="Teléfono" label="Teléfono" label-placement="floating" fill="solid"></ion-input>
            <ion-button expand="block" color="primary" @click="submitForm">Registrar</ion-button>
          </ion-card-content>
        </ion-card>
  ```
  # componente 3
  ```js
        <!-- Componente de Estadísticas -->
        <ion-card class="stats-card section">
          <ion-card-header>
            <ion-card-title>Estadísticas Generales</ion-card-title>
          </ion-card-header>
          <ion-card-content>
            <ion-grid>
              <ion-row>
                <ion-col>
                  <ion-label class="stat-title">Usuarios</ion-label>
                  <ion-badge color="primary">120</ion-badge>
                </ion-col>
                <ion-col>
                  <ion-label class="stat-title">Materias Activas</ion-label>
                  <ion-badge color="success">35</ion-badge>
                </ion-col>
              </ion-row>
              <ion-row>
                <ion-col>
                  <ion-label class="stat-title">Tareas Completadas</ion-label>
                  <ion-badge color="tertiary">450</ion-badge>
                </ion-col>
                <ion-col>
                  <ion-label class="stat-title">Proyectos</ion-label>
                  <ion-badge color="warning">5</ion-badge>
                </ion-col>
              </ion-row>
            </ion-grid>
          </ion-card-content>
        </ion-card>
      </ion-content>
    </ion-page>
  </template>

```





