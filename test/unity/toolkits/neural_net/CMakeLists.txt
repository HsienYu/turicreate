project(Turi)

make_boost_test(test_combine_base.cxx REQUIRES unity_shared_for_testing)
make_boost_test(test_combine_futures_subscriber.cxx REQUIRES unity_shared_for_testing)
make_boost_test(test_combine_iterator.cxx REQUIRES unity_shared_for_testing)
make_boost_test(test_combine_map.cxx REQUIRES unity_shared_for_testing)
make_boost_test(test_combine_queue.cxx REQUIRES unity_shared_for_testing)
make_boost_test(test_image_augmentation.cxx REQUIRES unity_shared_for_testing)
make_boost_test(test_model_spec.cxx REQUIRES unity_shared_for_testing)

make_boost_test(PosixTaskQueueTests.cxx REQUIRES unity_shared_for_testing)

if(APPLE)
  make_boost_test(GrandCentralDispatchQueueTests.cxx REQUIRES unity_shared_for_testing)
endif()

if(APPLE AND HAS_MPS AND NOT TC_BUILD_IOS)
  make_boost_test(test_mps_image_augmentation.cxx REQUIRES unity_shared_for_testing)
endif()
