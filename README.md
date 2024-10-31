# Documentación de Componentes en la Aplicación "Universidad"

Este documento describe los componentes principales de la página "Universidad", junto con sus propiedades, propósitos y estilos personalizados.

---

## Código Completo de la Página

```html
<template>
  <ion-page>
    <!-- -componente-Encabezado principal -->
    <ion-header :translucent="true">
      <ion-toolbar>
        <ion-title>Universidad</ion-title>
      </ion-toolbar>
    </ion-header>

    <!-- 1-componente- Contenido principal -->
    <ion-content :fullscreen="true" class="content-container">
      
      <!-- 2-componente-Barra de búsqueda -->
      <ion-searchbar class="spaced-item" color="primary" placeholder="Buscar"></ion-searchbar>

      <!-- 3-componente-Entrada de usuario -->
      <ion-input class="spaced-item" label="Usuario" label-placement="floating" fill="solid" placeholder="Ingrese usuario"></ion-input>

      <!-- 4-componente-Entrada de contraseña -->
      <ion-input class="spaced-item" label="Contraseña" label-placement="floating" fill="outline" placeholder="Ingrese contraseña"></ion-input>

      <!-- 5-componente-Selección de género -->
      <ion-list class="spaced-item">
        <ion-item>
          <ion-select placeholder="Seleccione un Género">
            <div slot="label">Género <ion-text color="danger">*</ion-text></div>
            <ion-select-option value="Masculino">Masculino</ion-select-option>
            <ion-select-option value="Femenino">Femenino</ion-select-option>
          </ion-select>
        </ion-item>
      </ion-list>

      <!-- 6-componente-Checkbox de acceso -->
      <ion-item class="spaced-item">
        <ion-checkbox slot="start" aria-label="Acceder"></ion-checkbox>
        <ion-label>Acceder</ion-label>
      </ion-item>

      <!-- 7-componente-Sección del menú -->
      <ion-toolbar class="menu-section">
        <ion-buttons slot="start">
          <ion-menu-button :auto-hide="false"></ion-menu-button>
        </ion-buttons>
        <ion-title>Menú</ion-title>
      </ion-toolbar>

      <!-- 8-componente-Tarjeta de Notificaciones -->
      <ion-card class="spaced-item">
        <ion-card-header>
          <ion-card-title>Notificación</ion-card-title>
          <ion-card-subtitle>Importante</ion-card-subtitle>
        </ion-card-header>
        <ion-card-content>
          Recuerda revisar las actividades pendientes para esta semana. Mantente al día con tus asignaciones.
        </ion-card-content>
      </ion-card>

      <!-- 9-componente-Listado de Mensajes Recientes -->
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

      <!-- 10-componente-Información de materias seleccionable -->
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
