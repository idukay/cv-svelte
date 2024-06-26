<script>
  import profileData from '$lib/assets/data/profile.json';
  import LeftSide from './LeftSide.svelte';
  import RightSide from './RightSide.svelte';
</script>

<div class="cv-template-1">
  <LeftSide {profileData} />
  <RightSide {profileData} />
</div>

<style>
  .cv-template-1 {
    display: flex;
    height: 100%;
  }
</style>