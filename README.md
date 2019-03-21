# ci_crud_model
Membuat CRUD Model Standar Pada Codeigniter

Cara Penggunannya

Load Model pada Controller atau masukan ke Autoload.php

$this->load->model(array('m_crud'));

Penggunaan Pada Controller

# Untuk Menampilkan data dari Table

$x['data'] = $this->m_crud->get('Nama_Table')->result();

# Untuk Update Data

$data = array(
  'field_database1' => $_POST['nama_field1'],
  'field_database2' => $_POST['nama_field2']
);

$this->m_crud->update('primary_key','idnya',$data,'Nama_Table');

# Untuk Insert Data
$data = array(
  'field_database1' => $_POST['nama_field1'],
  'field_database2' => $_POST['nama_field2']
);

$this->m_crud->insert($data,'Nama_Table');

# Untuk Delete Data
$id = 'IDnya';

$this->m_crud->del('Primary_key',$id,'Nama_Table');
