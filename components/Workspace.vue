<template>
  <v-autocomplete
        :items="workspaces"
        :filter="customFilter"
        color="secondary"
        item-text="name"
        hide-details=true
        style="max-width:300px"
        label="Workspace"
      ></v-autocomplete>
</template>

<script>
  export default {
    data () {
      return {
        hasSaved: false,
        isEditing: null,
        model: null,
        workspaces: [
          { name: "Pad Thai", owner: 'Fred', id: 1 },
          { name: "Lasagna", owner: 'Gustl', id: 2 },
          { name: "Halloumi", owner: 'Hans', id: 2 },
        ],
      }
    },

    methods: {
      customFilter (item, queryText, itemText) {
        const textOne = item.name.toLowerCase()
        const textTwo = item.owner.toLowerCase()
        const searchText = queryText.toLowerCase()

        return textOne.indexOf(searchText) > -1 ||
          textTwo.indexOf(searchText) > -1
      },
      save () {
        this.isEditing = !this.isEditing
        this.hasSaved = true
      },
    },
  }
</script>
