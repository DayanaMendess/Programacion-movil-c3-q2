<template>
    <ion-page>
      <ion-header>
        <ion-toolbar>
          <ion-title>Gestión y Estadísticas</ion-title>
        </ion-toolbar>
      </ion-header>
  
      <ion-content :fullscreen="true" class="content-container">
        
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
  
  <script setup lang="ts">
  // Funciones para el componente CRUD
  function createItem() {
    alert("Crear nuevo elemento");
  }
  function readItem() {
    alert("Leer información del elemento");
  }
  function updateItem() {
    alert("Actualizar elemento existente");
  }
  function deleteItem() {
    alert("Eliminar elemento");
  }
  
  // Función para el formulario de registro
  function submitForm() {
    alert("Formulario enviado");
  }
  </script>
  
  <style scoped>
  /* Contenedor principal del contenido */
  .content-container {
    padding: 16px; /* Espacio general alrededor del contenido */
  }
  
  /* Clase de sección para margen entre componentes */
  .section {
    margin-bottom: 400px;
  }
  
  /* Estilos para la tarjeta CRUD */
  .crud-card, .form-card, .stats-card {
    padding: 10px;
  }
  
  /* Estilos para el título de estadísticas */
  .stat-title {
    font-size: 14px;
    font-weight: bold;
    color: #666;
  }
  
  ion-badge {
    font-size: 16px;
    padding: 8px;
    margin-top: 8px;
    display: block;
  }
  </style>
  