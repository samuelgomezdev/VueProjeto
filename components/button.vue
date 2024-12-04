<template>
    <button
      :class="['fancy-button', buttonClass]"
      :type="type"
      
    >
      <span class="button-content">
        <slot>Meu botão</slot>
      </span>
      <span class="button-hover"></span>
    </button>
  </template>
  
  <script>
  export default {
    name: 'FancyButton',
    
    methods: {
      onClick(event) {
        this.$emit('click', event);
      },
    },
  };
  </script>
  
  <style scoped>
  .fancy-button {
    position: relative;
    display: inline-block;
    padding: 12px 20px;
    font-size: 16px;
    font-weight: 600;
    color: #ffffff;
    background: linear-gradient(90deg, #4facfe 0%, #00f2fe 100%);
    border: none;
    border-radius: 30px;
    cursor: pointer;
    overflow: hidden;
    outline: none;
    transition: transform 0.2s ease, box-shadow 0.3s ease;
  }
  
  .fancy-button:hover {
    transform: translateY(-2px);
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
  }
  
  .fancy-button:active {
    transform: translateY(0);
    box-shadow: none;
  }
  
  .fancy-button .button-content {
    position: relative;
    z-index: 2;
  }
  
  .fancy-button .button-hover {
    position: absolute;
    top: 0;
    left: -100%;
    width: 300%;
    height: 100%;
    background: rgba(255, 255, 255, 0.15);
    transform: skewX(-45deg);
    z-index: 1;
    transition: left 0.3s ease;
  }
  
  .fancy-button:hover .button-hover {
    left: -50%;
  }
  </style>
  