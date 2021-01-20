<template>
    <div class="container">
        <div class="card mx-auto shadow" style="width:24rem;">

            <div class="card-body">
                <h2>Sign in</h2>

                <form class="py-4">
                    <div class="form-row">
                        <div class="form-group col-md-12">
                            <label for="inputEmail4">Email</label>
                            <input type="email" class="form-control" id="inputEmail4" />
                        </div>
                        <div class="form-group col-md-12">
                            <label for="inputPassword4">Password</label>
                            <input type="password" class="form-control" id="inputPassword4" />
                        </div>


                        <div class="form-group col-md-12">
                            <button type="submit" class="btn btn-primary btn-block">Sign in</button>
                        </div>
                    </div>

                    <small>Forgot your password ?</small>
                </form>

            </div>

            <div class="card-footer bg-primary text-white text-center">
                <small>Don't have an account ? Sign up !</small>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    
};
</script>

<style lang="scss">
</style>