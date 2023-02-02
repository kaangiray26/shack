<template>
    <div id="createModal" class="modal fade" tabindex="-1">
        <div class="modal-dialog modal-dialog-centered">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title fw-bold">Create</h5>
                    <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                <div class="modal-body">
                    <p>Modal body text goes here.</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
import { ref, onMounted } from 'vue';
import { Modal } from 'bootstrap';

const modal = ref(null);

function show() {
    modal.value.show();
}

function hide() {
    modal.value.hide();
}

defineExpose({
    show,
    hide
})

onMounted(() => {
    modal.value = new Modal(document.querySelector('#createModal'), {
        backdrop: 'static',
        keyboard: false
    });
});
</script>