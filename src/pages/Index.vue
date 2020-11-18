<template>
  <q-page padding>
    <div class="row q-mb-lg">
      <q-input placeholder="Add new task" class="col"/>
      <q-btn
        color="primary"
        size="sm"
        label="Add"></q-btn>

    </div>
    <div class="row">
      <q-list bordered class="rounded-borders col">
        <q-item-label header>Tasks</q-item-label>
        <q-item v-for="(task, index) in tasks" v-bind:key="index">
          <q-item-section>
            <q-item-label class="col-2 gt-sm">
              {{task}}
            </q-item-label>
          </q-item-section>
          <q-item-section top side>
            <div class="text-grey-8 q-gutter-xs">
              <q-btn class="gt-xs" size="12px" flat dense round icon="delete" />
              <q-btn class="gt-xs" size="12px" color="green" flat dense round icon="done" />
            </div>
          </q-item-section>
        </q-item>
      </q-list>
    </div>
  </q-page>
</template>

<script>
export default {
  name: 'PageIndex',
  data () {
    return {
      tasks: ['Wake up', 'Brush teeth', 'Shower']
    }
  }
}
</script>
