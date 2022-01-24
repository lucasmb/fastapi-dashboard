<template>
  <div>
    <h1>USERS</h1>
    {{ users }}
  </div>
</template>

<script>
import { gql } from 'graphql-tag'

export default {
  data() {
    return {
      users: null,
    }
  },
  apollo: {
    users: gql`
      query {
        users {
          id
          email
          firstName
          lastName
          active
        }
      }
    `,
  },
}
</script>

<style></style>
