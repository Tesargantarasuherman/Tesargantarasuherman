$where['(
                EXISTS (select 1 from data_surat_disposisi dsd where dsd.id_surat_kirim = data_surat_kirim.id and dsd.dibuat_oleh = "' .  $this->data->info->user->id . '")
                OR data_surat_disposisi.hadir = true
                )'
            ] = null;
