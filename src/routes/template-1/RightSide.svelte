<script>
  export let profileData;
</script>

<div class="right-side">
  <h2>Resumen</h2>
  <hr />
  
  <div>{@html profileData.professionalInfo.summary}</div>

  <h2>Formación</h2>
  <hr />
  <p>{profileData.education.education}</p>

  <h2>Experiencia</h2>
</div>

<style>
  .right-side {
    flex: 2;
    background-color: #fff;
    padding: 20px;
  }
</style>