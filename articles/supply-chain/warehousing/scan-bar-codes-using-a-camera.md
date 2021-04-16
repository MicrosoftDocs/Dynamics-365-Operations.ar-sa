---
title: مسح الأكواد الشريطية باستخدام كاميرا في تطبيق إدارة المستودع للأجهزة المحمولة
description: يشرح هذا الموضوع كيفية إعداد تطبيق إدارة المستودع للأجهزة المحمولة لمسح الرموز الشريطية باستخدام كاميرا على جهاز محمول.
author: MarkusFogelberg
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 2f61f9c45b95b730a7f1743963658ec00abfbb56
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831208"
---
# <a name="scan-bar-codes-using-a-camera-in-the-warehouse-management-mobile-app"></a><span data-ttu-id="f49e1-103">مسح الأكواد الشريطية باستخدام كاميرا في تطبيق إدارة المستودع للأجهزة المحمولة</span><span class="sxs-lookup"><span data-stu-id="f49e1-103">Scan bar codes using a camera in the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f49e1-104">يشرح هذا الموضوع كيفية إعداد تطبيق إدارة المستودع للأجهزة المحمولة لمسح الرموز الشريطية باستخدام كاميرا على جهاز محمول.</span><span class="sxs-lookup"><span data-stu-id="f49e1-104">This topic explains how to set up the Warehouse Management mobile app to scan bar codes using a camera on a mobile device.</span></span>

## <a name="setup"></a><span data-ttu-id="f49e1-105">الإعداد</span><span class="sxs-lookup"><span data-stu-id="f49e1-105">Setup</span></span>

<span data-ttu-id="f49e1-106">في إعدادات العرض الخاصة بتطبيق إدارة المستودع للأجهزة المحمولة، يمكنك تحديد ما إذا كان ينبغي استخدام الكاميرا لمسح الرمز الشريطي.</span><span class="sxs-lookup"><span data-stu-id="f49e1-106">In the display settings of the Warehouse Management mobile app, you can select if the camera should be used for bar code scanning.</span></span> <span data-ttu-id="f49e1-107">إذا قمت بتمكين الخيار **استخدام الكاميرا كماسح ضوئي**، فيمكنك استخدام الكاميرا في كل حقل إدخال تم فيه تعيين وضع الإدخال المفضل إلى **مسح ضوئي**.</span><span class="sxs-lookup"><span data-stu-id="f49e1-107">If you enable **Use the camera as scanner**, you can use the camera on every input field that has the preferred input mode set to **Scanning**.</span></span>

<span data-ttu-id="f49e1-108">للتحكم في ما إذا كان يجب أن يكون حقل الإدخال قابلاً للمسح الضوئي، في صفحة **أسماء حقول تطبيق التخزين**، قم بتعيين **وضع الإدخال المفضل** إلى **مسح ضوئي**.</span><span class="sxs-lookup"><span data-stu-id="f49e1-108">To control whether an input field should be scannable, on the **Warehouse app field names** page, set **Preferred input mode** to **Scanning**.</span></span> <span data-ttu-id="f49e1-109">عند تحديد هذا الخيار، يمكن استخدام الكاميرا للمسح الضوئي في تطبيق إدارة المستودع للأجهزة المحمولة.</span><span class="sxs-lookup"><span data-stu-id="f49e1-109">When this option is selected, a camera can be used for scanning in the Warehouse Management mobile app.</span></span> <span data-ttu-id="f49e1-110">لمزيد من المعلومات، راجع [تكوين الحقول لتطبيق إدارة المستودع للأجهزة المحمولة](configure-app-field-names-priorities-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="f49e1-110">For more information, see [Configure fields for the Warehouse Management mobile app](configure-app-field-names-priorities-warehouse.md).</span></span>

## <a name="supported-bar-code-formats"></a><span data-ttu-id="f49e1-111">تنسيقات الأكواد الشريطية المدعومة</span><span class="sxs-lookup"><span data-stu-id="f49e1-111">Supported bar code formats</span></span>

<span data-ttu-id="f49e1-112">يتم اعتماد تنسيقات الأكواد الشريطية الأكثر شيوعًا، بما فيها الكود 128 والكود 39 والكود 93 والأكواد EAN-8 وEAN-13 وUPC-E وUPC-A وQR.</span><span class="sxs-lookup"><span data-stu-id="f49e1-112">The most common bar code formats are supported, including Code 128, Code 39, Code 93, EAN-8, EAN-13, UPC-E, UPC-A, and QR codes.</span></span>

## <a name="navigation"></a><span data-ttu-id="f49e1-113">التنقل</span><span class="sxs-lookup"><span data-stu-id="f49e1-113">Navigation</span></span>

<span data-ttu-id="f49e1-114">سيتم بدء صفحة الكاميرا في كل صفحة حيث تم تعيين **وحدة الإدخال المفضلة** إلى *مسح* لحقل الإدخال، وعندما تكون في صفحة الكاميرا، استخدم الخيارات التالية للتنقل:</span><span class="sxs-lookup"><span data-stu-id="f49e1-114">The camera page will be initiated on each page where the input field has its **Preferred input mode** set to *Scanning*, when you are on the camera page use the following options to navigate:</span></span>

- <span data-ttu-id="f49e1-115">حدد الزر السابق للرجوع إلى صفحة **المهمة والتفاصيل**.</span><span class="sxs-lookup"><span data-stu-id="f49e1-115">Select the back button to go back to the **Task and details** page.</span></span>
- <span data-ttu-id="f49e1-116">حدد القلم الرصاص في صفحة **المهمة والتفاصيل** للانتقال إلى الصفحة، حيث يمكنك كتابة الإدخال يدويًا.</span><span class="sxs-lookup"><span data-stu-id="f49e1-116">Select the pencil on the **Task and details** page to go to the page where you can type input manually.</span></span>
- <span data-ttu-id="f49e1-117">حدد الكاميرا في صفحة **المهمة والتفاصيل** للرجوع إلى صفحة الكاميرا.</span><span class="sxs-lookup"><span data-stu-id="f49e1-117">Select the camera on the **Task and details** page to go back to the camera page.</span></span>

<span data-ttu-id="f49e1-118">في صفحة الكاميرا، عند تحديد زر الكاميرا، سيظهر باهتًا أثناء محاولة تحديد الرمز الشريطي.</span><span class="sxs-lookup"><span data-stu-id="f49e1-118">On the camera page, when you select the camera button, it will appear dimmed while trying to identify a bar code.</span></span> <span data-ttu-id="f49e1-119">إذا لم يتم تحديد الرمز الشريطي في غضون 5 ثوانٍ، فستنتهي العملية وسيصبح زر الكاميرا متاحًا مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="f49e1-119">If a bar code is not identified within 5 seconds, the process will time out and the camera button will become available again.</span></span> <span data-ttu-id="f49e1-120">بعد ذلك، سيكون بإمكانك محاولة مسح كود شريطي مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="f49e1-120">You will then be able to try to scan a bar code again.</span></span>

<span data-ttu-id="f49e1-121">عندما تقوم بتوجيه الكاميرا نحو كود شريطي، اعمل على إبقاء الكود الشريطي في وضع المحاذاة داخل الأقواس للحصول على أفضل النتائج.</span><span class="sxs-lookup"><span data-stu-id="f49e1-121">When you aim the camera at a bar code, keep the bar code aligned within the brackets for best result.</span></span> <span data-ttu-id="f49e1-122">عندما يتم مسح كود شريطي بنجاح، ستتم معالجة النتيجة، وسيتم نقلك إلى الخطوة التالية.</span><span class="sxs-lookup"><span data-stu-id="f49e1-122">When a bar code is scanned successfully, the result will be processed, and you will be taken to the next step.</span></span> <span data-ttu-id="f49e1-123">إذا احتوت الخطوة التالية على حقل إدخال آخر تم فيه تعيين وضع الإدخال المفضل إلى "مسح ضوئي"، فستبدأ صفحة الكاميرا من جديد.</span><span class="sxs-lookup"><span data-stu-id="f49e1-123">If the next step contains another input field with the preferred input mode set to Scanning, the camera page will start again.</span></span> <span data-ttu-id="f49e1-124">إذا لم تكن الخطوة التالية عبارة عن حقل مسح، فلن تبدأ عندئذٍ صفحة الكاميرا.</span><span class="sxs-lookup"><span data-stu-id="f49e1-124">If the next step is not a scanning field, then the camera page will not be initiated.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]