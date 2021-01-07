<template>
    <div>
        <b-row class="my-3">
            <b-col cols="9">
                <form>
                    <b-card class="mb-3">
                        <b-form-group
                        label-for="house_name"
                        >
                            <b-form-input id="house_name" placeholder="Введите название проекта" trim></b-form-input>
                        </b-form-group>     
                        <b-form-group
                        label-for="short_description"
                        class="mb-0"
                        >
                            <b-form-input id="short_description" placeholder="Введите краткое описание проекта" trim></b-form-input>
                        </b-form-group>
                    </b-card>
                     <b-card no-body class="mb-3">
                        <b-tabs pills card vertical>
                            <b-tab title="Основные параметры" active>
                            
                                <b-form-group            
                                id="regular_price"
                                label-for="regular_price"
                                >
                                    <b-form-input type="number" id="regular_price" placeholder="Начальная стоимость" trim></b-form-input>
                                </b-form-group>
                                <b-form-group            
                                id="sail_price"
                                label-for="sail_price"
                                >
                                    <b-form-input type="number" id="sail_price" placeholder="Продажная стоимость" trim></b-form-input>
                                </b-form-group>

                            </b-tab>
                            <!-- <b-tab title="Inventory">
                            
                                <div class="form-group">
                                    <label for="stock_status">Кол-во квартир</label>
                                    <select class="form-control" id="stock_status">
                                    <option>In stock</option>
                                    <option>Out of stock</option>
                                    <option>On backorder</option>
                                    </select>
                                </div>
                                <b-form-group            
                                id="stock_quantity"
                                label-for="stock_quantity"
                                >
                                    <b-form-input type="number" id="stock_quantity" placeholder="Stock quantity" trim></b-form-input>
                                </b-form-group>
                                <b-form-group            
                                id="stock_quantity"
                                label-for="stock_quantity"
                                >
                                    <b-form-input type="number" id="stock_quantity" placeholder="Low stock threshold" trim></b-form-input>
                                </b-form-group>

                            </b-tab> -->
                            <b-tab title="Размеры">
                            
                                <b-form-group            
                                id="stock_quantity"
                                label-for="stock_quantity"
                                >
                                    <b-form-input type="number" id="stock_quantity" placeholder="Высота" class="mr-3 mb-3" trim></b-form-input>
                                    <b-form-input type="number" id="stock_quantity" placeholder="Ширина" class="mr-3 mb-3" trim></b-form-input>
                                    <b-form-input type="number" id="stock_quantity" placeholder="Длина" trim></b-form-input>
                                </b-form-group>
                            </b-tab>
                        </b-tabs>
                    </b-card>
                    <b-card>
                        <b-form-group
                        label-for="long_description"
                        >
                            <b-form-textarea id="long_description" placeholder="Введите описание проекта" trim style="min-height: 100px;"></b-form-textarea>
                        </b-form-group>
                    </b-card>
                </form>
            </b-col>
            <b-col cols="3"> 
                <form>    
                    <b-card class="mb-3">         
                        <b-button type="submit" block variant="primary">Добавить</b-button>
                    </b-card>
                    
                    <div class="card mb-3 p-3">
                        <b-form-group>
                            <b-form-file placeholder="Основное изображение" id="file-small" size="sm" style="width: 100%;"></b-form-file>
                        </b-form-group>
                        <img class="card-img-top" src="../../assets/images/jpg/no_image.jpg" style="height: 150px; object-fit:cover;">
                    </div>
                    
                    <div class="card mb-3 p-3">
                        <b-form-group>
                            <b-form-file placeholder="Галерея" id="file-small" size="sm" style="width: 100%;"></b-form-file>
                        </b-form-group>
                        <div class="d-flex flex-wrap">
                            <img class="card-img-top mr-2 mb-2" src="../../assets/images/jpg/no_image.jpg" style="width: 29%; object-fit:cover;">
                            <img class="card-img-top mr-2 mb-2" src="../../assets/images/jpg/no_image.jpg" style="width: 29%; object-fit:cover;">
                            <img class="card-img-top mr-2 mb-2" src="../../assets/images/jpg/no_image.jpg" style="width: 29%; object-fit:cover;">
                            <img class="card-img-top mr-2 mb-2" src="../../assets/images/jpg/no_image.jpg" style="width: 29%; object-fit:cover;">
                            <img class="card-img-top mr-2 mb-2" src="../../assets/images/jpg/no_image.jpg" style="width: 29%; object-fit:cover;">
                        </div>
                    </div>
                </form>
            </b-col>
        </b-row>
    </div>
</template>
