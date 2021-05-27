---
title: أدوات اختبار إدارة الجودة
description: يوضح هذا الموضوع كيفيه إنشاء مستندات الاختبار التي يمكن استخدامها لاختبارات الجودة علي أوامر الجودة في Microsoft Dynamics 365 Supply Chain Management.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestInstrument
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3806ca26b8909b03768dad54ddad0084e1cea4a6
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021722"
---
# <a name="quality-management-test-instruments"></a><span data-ttu-id="5f7d6-103">أدوات اختبار إدارة الجودة</span><span class="sxs-lookup"><span data-stu-id="5f7d6-103">Quality management test instruments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5f7d6-104">يوضح هذا الموضوع كيفيه إنشاء مستندات الاختبار التي يمكن استخدامها لاختبارات الجودة علي أوامر الجودة في Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5f7d6-104">This topic describes how to create test instruments that can be used for tests on quality orders in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="5f7d6-105">يمكنك استخدام صفحة **مستندات الاختبار** لتحديد وعرض التفاصيل حول الاجهزه التي يتم استخدامها لاجراء الاختبارات علي أوامر الجودة.</span><span class="sxs-lookup"><span data-stu-id="5f7d6-105">You use the **Test instruments** page to define and view details about the devices that are used to perform tests on quality orders.</span></span> <span data-ttu-id="5f7d6-106">مستندات الاختبارات اختيارية.</span><span class="sxs-lookup"><span data-stu-id="5f7d6-106">Test instruments are optional.</span></span> <span data-ttu-id="5f7d6-107">ومع ذلك، فانها يمكن ان تساعد العاملين في الجودة علي التعرف علي الجهاز أو الاداه التي يجب عليهم استخدامها لتنفيذ اختبار معين.</span><span class="sxs-lookup"><span data-stu-id="5f7d6-107">However, they can help quality workers know which device or tool they should use to perform a specific test.</span></span>

## <a name="test-instrument-example"></a><span data-ttu-id="5f7d6-108">مثال علي مستند الاختبار</span><span class="sxs-lookup"><span data-stu-id="5f7d6-108">Test instrument example</span></span>

<span data-ttu-id="5f7d6-109">أنت تقوم باجراء اختبارات متنوعة علي المكونات الكهربائية.</span><span class="sxs-lookup"><span data-stu-id="5f7d6-109">You're performing various tests on electrical components.</span></span> <span data-ttu-id="5f7d6-110">وتكون بعض الاختبارات الخاصة بإخراج الجهد الكهربي للمكونات، وكل اختبار لدرجه حرارتها، واختبار واحد لوزنها.</span><span class="sxs-lookup"><span data-stu-id="5f7d6-110">Some tests are for the voltage output of the components, one test is for their temperature, and one test is for their weight.</span></span> <span data-ttu-id="5f7d6-111">يتم استخدام أدوات أو أجهزة أو معدات مختلفة لإجراء كل اختبار.</span><span class="sxs-lookup"><span data-stu-id="5f7d6-111">Different tools, devices, or equipment is used to perform each test.</span></span> <span data-ttu-id="5f7d6-112">على سبيل المثال، يتم استخدام مقياس الجهد لقياس الجهد، ويستخدم مقياس حرارة لقياس درجة الحرارة، ويستخدم مقياس لقياس الوزن.</span><span class="sxs-lookup"><span data-stu-id="5f7d6-112">For example, a voltage meter is used to measure voltage, a thermometer is used to measure temperature, and a scale is used to measure weight.</span></span> <span data-ttu-id="5f7d6-113">يمكنك تكوين كل جهاز من هذه الأجهزة كأداة اختبار والإشارة إلى وحدة القياس التي يجب تسجيل نتائج الاختبار بها.</span><span class="sxs-lookup"><span data-stu-id="5f7d6-113">You can configure each of these devices as a test instrument and indicate the unit of measure that the test results should be recorded in.</span></span> <span data-ttu-id="5f7d6-114">على سبيل المثال، يتم تسجيل النتائج من مقياس الجهد بالفولت، ويتم تسجيل نتائج مقياس الحرارة بالدرجات فهرنهايت أو بالدرجات المئوية، ويتم تسجيل النتائج من المقياس بالجنيه أو الكيلوجرامات.</span><span class="sxs-lookup"><span data-stu-id="5f7d6-114">For example, results from the voltage meter are recorded in volts, results from the thermometer are recorded in degrees Fahrenheit or degrees Celsius, and results from the scale are recorded in pounds or kilograms.</span></span>

## <a name="create-a-test-instrument"></a><span data-ttu-id="5f7d6-115">إنشاء مستند اختبار</span><span class="sxs-lookup"><span data-stu-id="5f7d6-115">Create a test instrument</span></span>

1. <span data-ttu-id="5f7d6-116">انتقل إلى **إدارة المخزون \> الإعداد \> مراقبة الجودة \> مستندات الاختبارات**.</span><span class="sxs-lookup"><span data-stu-id="5f7d6-116">Go to **Inventory management \> Setup \> Quality control \> Test instruments**.</span></span>
1. <span data-ttu-id="5f7d6-117">في جزء الإجراءات، حدد **جديد** لإضافة صف إلى الشبكة.</span><span class="sxs-lookup"><span data-stu-id="5f7d6-117">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="5f7d6-118">ثم قم بتعيين الحقول التالية للصف الجديد:</span><span class="sxs-lookup"><span data-stu-id="5f7d6-118">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="5f7d6-119">**مستندات الاختبارات** – أدخل معرفا فريدا أو اسما فريدا لمستند الاختبار.</span><span class="sxs-lookup"><span data-stu-id="5f7d6-119">**Test instrument** – Enter a unique ID or name for the test instrument.</span></span>
    - <span data-ttu-id="5f7d6-120">**الوصف** - أدخل وصفًا مفصلاً لمستند الاختبار.</span><span class="sxs-lookup"><span data-stu-id="5f7d6-120">**Description** – Enter a detailed description of the test instrument.</span></span>
    - <span data-ttu-id="5f7d6-121">**الوحدة** - حدد الوحدة التي يقيس الجهاز النتائج فيها.</span><span class="sxs-lookup"><span data-stu-id="5f7d6-121">**Unit** – Select the unit that the instrument measures results in.</span></span> <span data-ttu-id="5f7d6-122">يتم تعيين حقل **الدقة** تلقائيا استنادا إلى الوحدة التي تقوم بتحديدها.</span><span class="sxs-lookup"><span data-stu-id="5f7d6-122">The **Precision** field is automatically set, based on the unit that you select.</span></span>

1. <span data-ttu-id="5f7d6-123">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="5f7d6-123">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5f7d6-124">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="5f7d6-124">Additional resources</span></span>

- [<span data-ttu-id="5f7d6-125">اختبار إدارة الجودة</span><span class="sxs-lookup"><span data-stu-id="5f7d6-125">Quality management test</span></span>](quality-tests.md)
- [<span data-ttu-id="5f7d6-126">مجموعات اختبارات إدارة الجودة</span><span class="sxs-lookup"><span data-stu-id="5f7d6-126">Quality management test groups</span></span>](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
