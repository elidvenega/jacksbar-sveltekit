<script>
    export let imageUrl;
    export let closeModal;
  
    function handleCloseModal() {
      closeModal();
    }
  </script>
  
  <div class="modal-overlay" on:click={handleCloseModal}>
    <div class="modal">
      <img src={imageUrl} alt="Modal Image" />
    </div>
  </div>
  
  <style>
    .modal-overlay {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0, 0, 0, 0.6);
      display: flex;
      justify-content: center;
      align-items: center;
      z-index: 999;
    }
  
    .modal {
      background-color: #fff;
      padding: 20px;
      box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
    }
  
    img {
      max-width: 100%;
      height: auto;
    }
  </style>
  