INSERT INTO chaincodes (
  chaincode_ref,
  type,
  full_blob,
  metadata,
  device_binding,
  biometric_hash,
  created_at,
  updated_at
)
VALUES (
  '9753ec1f', -- your generated 4-byte chaincode ref
  'org',      -- entity type
  DECODE('010100005f5457c99cdec6d7568b17d9e1465f4de94d343200000000000000000000000000000000ffffffffffffffff000000007b2c7ad90000000000000000', 'hex'), -- 64-byte blob
  '{"org_name": "JD Plumbing", "ein": "33-4243369", "license": "CFC#1428158", "state": "FL", "address": "11351 NW 31st Street, Sunrise, FL 33323"}',
  NULL,
  NULL,
  NOW(),
  NOW()
);
