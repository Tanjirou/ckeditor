### Código para /static/pages/css/custom_editor.css:

.django-ckeditor-widget, .cke_editor_id_content {
    width: 100% !important;
    max-width: 821px;
}

### Código para el admin.py

class PageAdmin(admin.ModelAdmin):
    list_display = ('title', 'order')
    
    # Inyectamos nuestro fichero css
    class Media:
        css = {
            'all': ('pages/css/custom_ckeditor.css',)
        }