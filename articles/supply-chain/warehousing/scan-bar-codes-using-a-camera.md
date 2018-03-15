---
title: "مسح الأكواد الشريطية باستخدام الكاميرا في Dynamics 365 for Finance and Operations – Warehousing"
description: "يشرح هذا الموضوع كيفية إعداد Dynamics 365 for Finance and Operations – Warehousing لمسح الأكواد الشريطية باستخدام كاميرا على جهاز محمول."
author: MarkusFogelberg
manager: AnnBe
ms.date: 01/03/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: ffbd853c15e479fc4350a19121f2aebcedda9854
ms.openlocfilehash: 31b9d421f3fd5378f26faeee3a83b66861ef5008
ms.contentlocale: ar-sa
ms.lasthandoff: 03/02/2018

---

# <a name="scan-bar-codes-using-a-camera-in-dynamics-365-for-finance-and-operations--warehousing"></a><span data-ttu-id="b4ffc-103">مسح الأكواد الشريطية باستخدام الكاميرا في Dynamics 365 for Finance and Operations – Warehousing</span><span class="sxs-lookup"><span data-stu-id="b4ffc-103">Scan bar codes using a camera in Dynamics 365 for Finance and Operations – Warehousing</span></span>

<span data-ttu-id="b4ffc-104">يشرح هذا الموضوع كيفية إعداد Dynamics 365 for Finance and Operations – Warehousing لمسح الأكواد الشريطية باستخدام كاميرا على جهاز محمول.</span><span class="sxs-lookup"><span data-stu-id="b4ffc-104">This topic explains how to set up Dynamics 365 for Finance and Operations – Warehousing to scan bar codes using a camera on a mobile device.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="b4ffc-105">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="b4ffc-105">Prerequisites</span></span>
<span data-ttu-id="b4ffc-106">لاستخدام هذه الميزة، يجب أن يكون الإصدار 1.2.0.0 من تطبيق Warehousing مثبتًا لديك، ويجب أن يتضمن جهازك كاميرا.</span><span class="sxs-lookup"><span data-stu-id="b4ffc-106">To use this feature, you need to have version 1.2.0.0 of Warehousing installed, and your device must have a camera.</span></span> <span data-ttu-id="b4ffc-107">عندما تفتح التطبيق بعد التحديث، سيتم مطالبتك بالسماح لتطبيق Dynamics 365 for Finance and Operations – Warehousing باستخدام الكاميرا.</span><span class="sxs-lookup"><span data-stu-id="b4ffc-107">When you open the app after updating, you will be prompted to allow the Dynamics 365 for Finance and Operations – Warehousing application to use the camera.</span></span> <span data-ttu-id="b4ffc-108">في حال عدم وجود كاميرا في جهازك، لن تظهر أي مطالبة، وسيتعذر عليك استخدام الكاميرا كماسح ضوئي.</span><span class="sxs-lookup"><span data-stu-id="b4ffc-108">If your device doesn’t have a camera, no prompt will be shown, and you will not be able to use a camera as a scanner.</span></span> 

## <a name="setup"></a><span data-ttu-id="b4ffc-109">إعداد</span><span class="sxs-lookup"><span data-stu-id="b4ffc-109">Setup</span></span>
<span data-ttu-id="b4ffc-110">في "إعدادات العرض" الخاصة بالتطبيق Warehousing، يمكنك تحديد ما إذا كان يجب استخدام الكاميرا لمسح الأكواد الشريطية.</span><span class="sxs-lookup"><span data-stu-id="b4ffc-110">In the Display settings of the Warehousing application, you can select if the camera should be used for bar code scanning.</span></span> <span data-ttu-id="b4ffc-111">إذا قمت بتمكين الخيار **استخدام الكاميرا كماسح ضوئي**، فيمكنك استخدام الكاميرا في كل حقل إدخال تم فيه تعيين وضع الإدخال المفضل إلى **مسح ضوئي**.</span><span class="sxs-lookup"><span data-stu-id="b4ffc-111">If you enable **Use the camera as scanner**, you can use the camera on every input field that has the preferred input mode set to **Scanning**.</span></span> 

<span data-ttu-id="b4ffc-112">للتحكم في ما إذا كان يجب أن يكون حقل الإدخال قابلاً للمسح الضوئي، في صفحة **أسماء حقول تطبيق المستودع‬** في Dynamics 365 for Finance and Operations، قم بتعيين **وضع الإدخال المفضل** إلى **مسح ضوئي**.</span><span class="sxs-lookup"><span data-stu-id="b4ffc-112">To control whether an input field should be scannable, on the **Warehouse app field names** page in Dynamics 365 for Finance and Operations, set **Preferred input mode** to **Scanning**.</span></span> <span data-ttu-id="b4ffc-113">عند تحديد هذا الخيار، يمكن استخدام كاميرا لإجراء مسح ضوئي في تطبيق Warehousing.</span><span class="sxs-lookup"><span data-stu-id="b4ffc-113">When this option is selected, a camera can be used for scanning in the Warehousing app.</span></span> <span data-ttu-id="b4ffc-114">لمزيد من المعلومات حول كيفية تكوين أسماء حقول التطبيق في Warehousing، راجع [تكوين أسماء حقول التطبيق في تطبيق Warehousing](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).</span><span class="sxs-lookup"><span data-stu-id="b4ffc-114">For information about how to configure app field names in Warehousing, see [Configure app field names in Warehousing app](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).</span></span>

## <a name="supported-bar-code-formats"></a><span data-ttu-id="b4ffc-115">تنسيقات الأكواد الشريطية المدعومة</span><span class="sxs-lookup"><span data-stu-id="b4ffc-115">Supported bar code formats</span></span>
<span data-ttu-id="b4ffc-116">يتم اعتماد تنسيقات الأكواد الشريطية الأكثر شيوعًا، بما فيها الكود 128 والكود 39 والكود 93 والأكواد EAN-8 وEAN-13 وUPC-E وUPC-A وQR.</span><span class="sxs-lookup"><span data-stu-id="b4ffc-116">The most common bar code formats are supported, including Code 128, Code 39, Code 93, EAN-8, EAN-13, UPC-E, UPC-A, and QR codes.</span></span> 

## <a name="navigation"></a><span data-ttu-id="b4ffc-117">التنقل</span><span class="sxs-lookup"><span data-stu-id="b4ffc-117">Navigation</span></span>
<span data-ttu-id="b4ffc-118">سيتم بدء صفحة الكاميرا على كل صفحة حيث تم تعيين وضع الإدخال المفضل لحقل الإدخال إلى "مسح ضوئي". عند وجودك في صفحة الكاميرا، استخدم الخيارات التالية للتنقل:</span><span class="sxs-lookup"><span data-stu-id="b4ffc-118">The camera page will be initiated on each page where the input field has the preferred input mode set to Scanning, when you are on the Camera page use the following options to navigate:</span></span>
- <span data-ttu-id="b4ffc-119">انقر فوق زر السابق للعودة إلى صفحة "المهمة والتفاصيل".</span><span class="sxs-lookup"><span data-stu-id="b4ffc-119">Click the back button to go back to the Task and details page.</span></span> 
- <span data-ttu-id="b4ffc-120">انقر فوق القلم في صفحة "المهمة والتفاصيل" للانتقال إلى الصفحة حيث يمكنك كتابة الإدخال يدويًا.</span><span class="sxs-lookup"><span data-stu-id="b4ffc-120">Click the pencil on the Task and details page to go to the page where you can type input manually.</span></span>
- <span data-ttu-id="b4ffc-121">انقر فوق الكاميرا في الصفحة "المهمة والتفاصيل" للرجوع إلى صفحة الكاميرا.</span><span class="sxs-lookup"><span data-stu-id="b4ffc-121">Click the camera on the Task and details page to go back to the Camera page.</span></span> 

| <span data-ttu-id="b4ffc-122">صفحة المهمة والتفاصيل</span><span class="sxs-lookup"><span data-stu-id="b4ffc-122">Task and details page</span></span> | <span data-ttu-id="b4ffc-123">صفحة الكاميرا</span><span class="sxs-lookup"><span data-stu-id="b4ffc-123">Camera page</span></span> | 
| --------------------- | -------------------- |
| ![camera-scanning-example-task-detail-page](media/camera-scanning-example-task-detail-page.png)          | ![camera-scanning-example-camera-page](media/camera-scanning-example-camera-page.png)          |

<span data-ttu-id="b4ffc-126">في صفحة الكاميرا، عندما تنقر فوق زر "الكاميرا"، سوف يظهر خافتًا أثناء محاولة تحديد كود شريطي.</span><span class="sxs-lookup"><span data-stu-id="b4ffc-126">On the camera page, when you click the Camera button, it will appear dimmed while trying to identify a bar code.</span></span> <span data-ttu-id="b4ffc-127">إذا لم يتم تحديد كود شريطي في غضون 5 ثوان، فستنتهي مهلة العملية وسيصبح زر الكاميرا متوفرًا من جديد.</span><span class="sxs-lookup"><span data-stu-id="b4ffc-127">If a bar code is not identified within 5 seconds, the process will time out and the Camera button will become available again.</span></span> <span data-ttu-id="b4ffc-128">بعد ذلك، سيكون بإمكانك محاولة مسح كود شريطي مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="b4ffc-128">You will then be able to try to scan a bar code again.</span></span>

<span data-ttu-id="b4ffc-129">عندما تقوم بتوجيه الكاميرا نحو كود شريطي، اعمل على إبقاء الكود الشريطي في وضع المحاذاة داخل الأقواس للحصول على أفضل النتائج.</span><span class="sxs-lookup"><span data-stu-id="b4ffc-129">When you aim the camera at a bar code, keep the bar code aligned within the brackets for best result.</span></span> <span data-ttu-id="b4ffc-130">عندما يتم مسح كود شريطي بنجاح، ستتم معالجة النتيجة، وسيتم نقلك إلى الخطوة التالية.</span><span class="sxs-lookup"><span data-stu-id="b4ffc-130">When a bar code is scanned successfully, the result will be processed, and you will be taken to the next step.</span></span> <span data-ttu-id="b4ffc-131">إذا احتوت الخطوة التالية على حقل إدخال آخر تم فيه تعيين وضع الإدخال المفضل إلى "مسح ضوئي"، فستبدأ صفحة الكاميرا من جديد.</span><span class="sxs-lookup"><span data-stu-id="b4ffc-131">If the next step contains another input field with the preferred input mode set to Scanning, the camera page will start again.</span></span> <span data-ttu-id="b4ffc-132">إذا لم تكن الخطوة التالية عبارة عن حقل مسح، فلن تبدأ عندئذٍ صفحة الكاميرا.</span><span class="sxs-lookup"><span data-stu-id="b4ffc-132">If the next step is not a scanning field, then the camera page will not be initiated.</span></span>


