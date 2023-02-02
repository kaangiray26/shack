<template>
    <div class="container h-100 d-flex align-items-center">
        <div class="row w-100 g-0 justify-content-center">
            <div class="col-12 col-lg-6">
                <div class="card shadow-lg border-dark">
                    <div class="card-body">
                        <div class="d-flex flex-column">
                            <div>
                                <img src="favicon.svg" class="img-fluid" width="64" height="64" />
                            </div>
                            <h1 class="fw-bold">Shack</h1>
                            <p>Create private chatrooms</p>
                            <button class="btn btn-outline-dark" type="button" @click="create_room">Create a
                                room</button>
                            <div class="d-flex flex-column mt-4">
                                <div class="mb-2">
                                    <button type="button" class="btn btn-sm btn-dark bi bi-github">
                                        <span class="ms-1">GitHub</span>
                                    </button>
                                </div>
                                <div>
                                    <button type="button" class="btn btn-sm btn-dark bi bi-github">
                                        <span class="ms-1">Created by kaangiray26</span>
                                    </button>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <Create ref="create_modal" />
</template>

<script setup>
import { ref, onMounted } from 'vue';
import { useRouter } from 'vue-router';
import Create from './Create.vue';

const router = useRouter();
const create_modal = ref(null);

function create_room() {
    create_modal.value.show();
}
</script>