---
title: قوالب الخدمة
description: يُمكنك تحديد اتفاقية خدمة كقالب ثم نسخ بنود القالب فيما بعد إلى اتفاقية خدمة أخرى أو إلى أمر خدمة.
author: ShylaThompson
manager: tfehr
ms.date: 02/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a8a92d67afe5fd427d1bc272c59e459cb1547d22
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4421049"
---
# <a name="service-templates"></a><span data-ttu-id="2143c-103">قوالب الخدمة</span><span class="sxs-lookup"><span data-stu-id="2143c-103">Service templates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2143c-104">يُمكنك تحديد اتفاقية خدمة كقالب ثم نسخ بنود القالب فيما بعد إلى اتفاقية خدمة أخرى أو إلى أمر خدمة.</span><span class="sxs-lookup"><span data-stu-id="2143c-104">You can define a service agreement as a template and copy the lines of the template later into another service agreement or into a service order.</span></span>

## <a name="example"></a><span data-ttu-id="2143c-105">مثال</span><span class="sxs-lookup"><span data-stu-id="2143c-105">Example</span></span>

<span data-ttu-id="2143c-106">يمتلك العميل الذي تقدم له الخدمة مصاعد خدمة متطابقة في خمسة مواقع مختلفة.</span><span class="sxs-lookup"><span data-stu-id="2143c-106">A customer for whom you provide service has identical service elevators at five different locations.</span></span>

<span data-ttu-id="2143c-107">ترغب في إعداد خمس اتفاقيات خدمة للعميل، بمعدل اتفاقية لكل موقع.</span><span class="sxs-lookup"><span data-stu-id="2143c-107">You want to set up five service agreements for the customer, one for each site.</span></span>
<span data-ttu-id="2143c-108">وللحد من تكرار الإعدادات، وللتأكد من تطابق معلومات الإعداد في اتفاقيات الخدمة، فإنك تقوم بإنشاء اتفاقية خدمة وتحديدها كقالب لعمل الخدمة على المصاعد.</span><span class="sxs-lookup"><span data-stu-id="2143c-108">To limit repetitive setup work, and to make sure that the setup information in the service agreements is identical, you create a service agreement and specify it as a template for the service work on the elevators.</span></span>

<span data-ttu-id="2143c-109">يُمكنك الآن نسخ بنود القالب إلى اتفاقيات الخدمة الخمس الجديدة، بحيث تتم تعبئة كل اتفاقية خدمة بالبنود من القالب.</span><span class="sxs-lookup"><span data-stu-id="2143c-109">You can now copy the template lines into the five new service agreements, so that each service agreement is populated with the lines from the template.</span></span>

## <a name="create-a-template"></a><span data-ttu-id="2143c-110">إنشاء قالب</span><span class="sxs-lookup"><span data-stu-id="2143c-110">Create a template</span></span>

<span data-ttu-id="2143c-111">عندما تنشئ قالب خدمة، سوف تنشئ اتفاقية خدمة وإنشاء البنود المطلوبة عليها، ثم إرفاق اتفاقية الخدمة بمجموعة قوالب الخدمة.</span><span class="sxs-lookup"><span data-stu-id="2143c-111">When you create a service template, you create a service agreement, create the required lines on it, and attach the service agreement to a service-template group.</span></span>

> [!NOTE]
> <span data-ttu-id="2143c-112">يمكن تعريف اتفاقية الخدمة كقالب فقط في حال عدم إرفاق أي أوامر خدمة بها.</span><span class="sxs-lookup"><span data-stu-id="2143c-112">A service agreement can be defined as a template only if it has no service orders attached to it.</span></span> <span data-ttu-id="2143c-113">علاوةً على ذلك، لا يُمكن إنشاء أوامر خدمة من اتفاقية خدمة تم تحديها كقالب.</span><span class="sxs-lookup"><span data-stu-id="2143c-113">Also, no service orders can be generated from a service agreement that is defined as a template.</span></span>

## <a name="copy-template-lines"></a><span data-ttu-id="2143c-114">نسخ بنود القالب</span><span class="sxs-lookup"><span data-stu-id="2143c-114">Copy template lines</span></span>

<span data-ttu-id="2143c-115">يُمكنك نسخ بنود القالب من قالب خدمة إلى اتفاقية خدمة أخرى أو إلى أمر خدمة.</span><span class="sxs-lookup"><span data-stu-id="2143c-115">You can copy template lines from a service template into another service agreement or into a service order.</span></span>

<span data-ttu-id="2143c-116">عندما تقوم بنسخ بنود قالب إلى أوامر الخدمة أو اتفاقيات الخدمة، تظهر مجموعة القوالب في طريقة عرض شجرة حيث يُمكن توسيع كل مجموعة.</span><span class="sxs-lookup"><span data-stu-id="2143c-116">When you copy template lines into your service orders or service agreements, your template groups are displayed in a tree view in which each group can be expanded.</span></span> <span data-ttu-id="2143c-117">ويُتيح لك هذا عرض كل قالب وبند قالب.</span><span class="sxs-lookup"><span data-stu-id="2143c-117">This display lets you view each template and template line.</span></span>

<span data-ttu-id="2143c-118">ويصبح من الأسهل تحديد بنود قالب الخدمة التي تريد نسخها إذا قمت بتجميع القوالب بأسماء تعكس استخدام القوالب.</span><span class="sxs-lookup"><span data-stu-id="2143c-118">It is easier to determine the service-template lines that you want to copy if you have grouped the templates under names that reflect the use of the templates.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2143c-119">مواضيع مرتبطة</span><span class="sxs-lookup"><span data-stu-id="2143c-119">Related topics</span></span>

[<span data-ttu-id="2143c-120">نسخ بنود قوالب خدمة</span><span class="sxs-lookup"><span data-stu-id="2143c-120">Copy service templates lines</span></span>](copy-service-template-lines.md)
