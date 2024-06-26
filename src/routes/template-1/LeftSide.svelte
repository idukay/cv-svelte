<script>
  import FaMapMarkerAlt from 'svelte-icons/fa/FaMapMarkerAlt.svelte';
  import FaMobileAlt from 'svelte-icons/fa/FaMobileAlt.svelte';
  import IoIosMail from 'svelte-icons/io/IoIosMail.svelte';
  import profilePicture from '$lib/assets/images/roberto_ruiz.jpg';

  import Icon from '@/components/Icon.svelte';

  export let profileData;
</script>

<div class="left-side">
  <div class="profile-picture">
    <img src={profilePicture} alt="" width="200">
  </div>

  <div class="introduce">
    <h1>
      {profileData.name}
      <br />
      {profileData.lastName}
    </h1>
    <p>{profileData.professionalInfo.profession}</p>
    <p><i>{profileData.professionalInfo.position}</i></p>
  </div>

  <div class="contact-info">
    <ul>
      <li>
        <Icon size="20" color="white"><FaMapMarkerAlt /></Icon>
        <i>{profileData.addressInfo.city}, {profileData.addressInfo.country}</i>
      </li>
      <li>
        <Icon size="20" color="white"><IoIosMail /></Icon>
        <i>{profileData.contactInfo.email}</i>
      </li>
      <li>
        <Icon size="20" color="white"><FaMobileAlt /></Icon>
        <i>{profileData.contactInfo.phone}</i>
      </li>
    </ul>
  </div>
</div>

<style>
  .left-side {
    flex: 1;
    background-color: #222;
    padding: 40px 10px;
    color: white;

    & .profile-picture {
      display: flex;
      justify-content: center;
      
      & img {
        border-radius: 50%;
      }
    }

    & .contact-info {
        flex: 1;
        font-style: italic;

        & ul {
          margin: 0;
          padding: 0;
          list-style: none;

          & li {
            display: flex;
            margin-bottom: 7px;

            & i {
              margin-left: 7px;
            }
          }
        }
      }
  }
</style>